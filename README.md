# ProjectRecommenderSystem_HUST
## Các thư viện sử dụng
- Panda
- Numpy
- Python == 3.8
- Torch
- Pytorch
- cuda == 11.8.0
## Các files quan trọng
- Baseline (Private score: 0.48812 - Public score: 0.48677): Rerank_baseline.ipynb , chứa mã nguồn baseline model
- Word2vec (Private score: 0.51245 - Public score: 0.51236): test_W2v.ipynb, chứa mã nguồn Word2vec (cho độ dài chuỗi items bất kỳ). Ngoài ra dựa trên mã nguồn này, nếu chỉ sử dụng word2vec cho chuỗi có độ dài ít hơn 20 thì (Private score: 0.52185 - Public score: 0.52138)
- GNN (Private score: 0.00016 - Public score: 0.00016): GNN thử nghiệm
  - Xây dựng Graph data: Node-Graph-Creating.ipynb
  - Huấn luyện GNN: Trainning-GNN.ipynb
  - Gợi ý: Inference.ipynb
- (chạy trên kaggle) Handrules (Private score: 0.57529 - Public score: 0.57549): candidate-rerank-handcrafted-rules.ipynb 
- (chạy trên kaggle) Gru4rec (Private score: 0.54418 - Public score: 0.54465): gru4rec.ipynb 
  
## Quan sát và kết luận
- Baseline dựa trên quan sát chuỗi dài và càng phía cuối chuỗi thì các item càng được mua. Tuy nhiên, cách này nhạy cảm với item ngoại lai, và ở xa nên trọng số của click dù thấp vẫn khá cao.
- Word2vec tập trung chọn ra những items gần nhau trong chuỗi, tuy nhiên chuỗi càng dài thì word2vec không tốt.
- GRU4rec có thể khắc phục nhược điểm của Word2vec.
  

