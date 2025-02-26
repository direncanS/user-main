bu kod da ister lambda ister ec2 olarak deploy edilebilir. 
lambda olarak yapilirsa onunne api-gateway lazim ayni api-gateway kullanilabilir webcam-api ile. 

```
r.HandleFunc("/images", handlers.GetDataTopics).Methods("GET")
	r.HandleFunc("/images/{topic}", handlers.GetByTopic).Methods("GET")
	r.HandleFunc("/videos", handlers.GetVideosByTopic).Methods("GET")
	r.HandleFunc("/videos/{folder}", handlers.GetVideoFromFolder).Methods("GET")
```

bu endpoint leri bu lambda ya api-gateway uzerinden map edebilirsin. 

