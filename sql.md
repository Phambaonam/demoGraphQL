1. chọn ra bài viết dc nhiều tác giả viết nhất.
```sql
    select author_post.post_id , count(*)  as count from author
    join author_post on author.id = author_post.author_id
    group by  author_post.post_id  order by count DESC limit 1
```

2. tìm 3 tác giả có nhiều bài viết nhất.
```sql
    select author_post.author_id, count(*) as count from author_post
    join post on author_post.post_id = post.id
    group by author_post.author_id order by count DESC limit 3
```

3. tìm ra thông tin đầy đủ của tác giả và tất cả các bài viêt của họ.
```sql
   ﻿select * from author
   	join author_post on author.id = author_post.author_id
    join post on author_post.post_id = post.id
    where author_post.post_id = post.id and author_post.author_id = 3
```

4.