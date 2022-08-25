---
layout: post
title: 리사이클러뷰(RecyclerView)에서 파이어스토어(Firestore) 데이터 받기
subtitle: ChatApp 토이 프로젝트
categories: Android
tags: Android Java Chat Firebase Firestore
---

오늘 파이어스토어를 사용하며 고생한 부분을 기록하고자 한다. 우선 프로젝트에서 리사이클러뷰를 사용하고 파이어스토어에 데이터까지 업로드가 마친 상태를 가정한다. 그 후 데이터를 받아와 보여주는 방법에 대해 설명한다.

```java
YourActivity {
        // 1. 우선 리사이클러뷰가 있는 액티비티에 파이어스토어를 객체를 생성하고 인스턴스를 받는다.
        FirebaseFirestore db = FirebaseFirestore.getInstance();
    onCreate(){
        // 2. 데이터를 받을 User 타입의 ArrayList를 만들어준다.
        ArrayList<User> users = new ArrayList<>();

        // 3. 그 후 onCreate() 메서드 내부에서 get()를 이용하여 데이터를 받는다. 
        db.collection("users")
          .get()
          .addOnCompleteListener(task -> {
              if(task.isSuccessful()){
                for(DocumentSnapshot document : task.getResult().getDocuments()){
                    // toObject() 메서드를 이용하여 요소들을 User 클래스로 변환시켜 넣는다.
                    users.add(document.toObject(User.class))
                    // notifyDataSetChanged() 메서드를 사용해 정보를 업데이트한다.
                    adapter.notifyDataSetChanged();
                }
            } else {
                Log.e(TAG, "error")
            }
        }
    }


}
```
