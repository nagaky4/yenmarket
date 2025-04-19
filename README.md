# Câu hỏi:

Nếu API trả về chậm, bạn sẽ debug và tối ưu cách nào để cải thiện tốc độ load?

# Câu trả lời

1.Để debug:
-để kiểm tra api nào chậm trễ, thời gian phản hồi là bao lâu,
dùng chromedevtool mở tab nextwork, hoặc dùng postman
-dùng nuxtdevtool
-dùng log

2.Để cải thiện tốc độ load:
-dùng CDN
-cache response
-dùng lazy load
-dùng hình ảnh dạng WebP hoặc svg
-chỉ lấy những field trong reponse cần thiết thay vì trả về hết object
ví dụ response của product chỉ cần trả về: [{image:'', title:'', price: ''}]
