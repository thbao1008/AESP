# ĐỀ TÀI: XÂY DỰNG NỀN TẢNG HỖ TRỢ GIÁO DỤC ỨNG DỤNG TRÍ TUỆ NHÂN TẠO (AESP)

Tên tiếng Anh: Development of an AI Education Support Platform (AESP)

## 1. CHỐT ĐỀ TÀI, PHẠM VI VÀ KẾT QUẢ ĐẦU RA

### 1.1. Tên đề tài

Xây dựng nền tảng hỗ trợ giáo dục ứng dụng trí tuệ nhân tạo (AI Education Support Platform – AESP).

### 1.2. Mô tả đề tài

AESP là hệ thống phần mềm hỗ trợ học tập ứng dụng trí tuệ nhân tạo, hướng đến việc nâng cao khả năng tự học và cải thiện trải nghiệm học tập của người dùng. Hệ thống tích hợp AI vào các hoạt động học tập, giúp người học thực hành, tương tác, nhận phản hồi và theo dõi tiến độ học tập. Bên cạnh đó, hệ thống cung cấp các chức năng hỗ trợ cộng đồng để người học có thể trao đổi và nhận sự hỗ trợ từ Mentor khi cần thiết.

Hệ thống được thiết kế với bốn vai trò chính gồm Admin, AI, Mentor và Learner. Trong đó, AI là tác nhân hỗ trợ học tập chính; Mentor đảm nhiệm vai trò hỗ trợ, giải đáp thắc mắc và theo dõi tiến độ của người học được phân công; Admin chịu trách nhiệm quản lý hệ thống; Learner chủ động học tập và luyện tập với AI.

### 1.3. Bài toán cần giải quyết

Quá trình học tập cần có phương thức hỗ trợ người học luyện tập chủ động, tiếp nhận phản hồi và theo dõi sự tiến bộ. Nếu việc học phụ thuộc quá nhiều vào sự hướng dẫn trực tiếp của con người, người học có thể gặp khó khăn khi muốn luyện tập thường xuyên hoặc cần phản hồi kịp thời.

AESP hướng đến giải quyết bài toán này thông qua việc ứng dụng AI để hỗ trợ các hoạt động học tập, cung cấp phản hồi dựa trên kết quả thực hiện và hỗ trợ theo dõi tiến độ. Đồng thời, hệ thống vẫn duy trì vai trò hỗ trợ của Mentor và cung cấp công cụ quản lý tập trung cho Admin.

### 1.4. Mục tiêu của đề tài

- Xây dựng hệ thống học tập có tích hợp AI.
- Hỗ trợ người học luyện tập, tương tác và tiếp nhận phản hồi từ AI.
- Hỗ trợ theo dõi kết quả và tiến độ học tập.
- Xây dựng chức năng hỗ trợ học tập và trao đổi cộng đồng cho Mentor và Learner.
- Phân định rõ quyền hạn của từng vai trò.
- Đảm bảo dữ liệu được quản lý nhất quán và quyền truy cập được kiểm soát tại backend.

### 1.5. Phạm vi đề tài

**Phạm vi chức năng dự kiến:**

1. Quản lý tài khoản, xác thực và phân quyền.
2. Cung cấp các hoạt động học tập, luyện tập và tương tác với AI.
3. Phân tích kết quả, cung cấp phản hồi và hỗ trợ theo dõi tiến độ.
4. Hỗ trợ trao đổi trong cộng đồng học tập.
5. Cho phép Mentor giải đáp thắc mắc, theo dõi người học được phân công và hỗ trợ khi cần.
6. Cung cấp chức năng quản lý người dùng, quyền hạn và hoạt động hệ thống cho Admin.
7. Xây dựng và kiểm thử các thành phần frontend, backend, API và cơ sở dữ liệu.

**Giới hạn của đề tài:**

- Tập trung vào việc ứng dụng các mô hình hoặc dịch vụ AI có sẵn, không mặc định phải tự huấn luyện một mô hình nền tảng mới.
- Không cam kết AI luôn đưa ra kết quả chính xác tuyệt đối.

  
### 1.6. Kết quả đầu ra dự kiến (Deliverables)

- Mã nguồn dự án AESP được tổ chức và quản lý trên Git.
- Hệ thống frontend và backend có khả năng tích hợp các chức năng theo phạm vi đã thống nhất.
- Cơ sở dữ liệu và cấu trúc lưu trữ phù hợp với các luồng nghiệp vụ.
- Chức năng học tập với AI, hỗ trợ học tập và quản lý hệ thống theo phạm vi thực tế.
- Bộ kiểm thử chức năng, API, phân quyền và tích hợp.
- Tài liệu SRS, WBS, thiết kế hệ thống, mô hình dữ liệu và hướng dẫn cài đặt/chạy ứng dụng.
- Báo cáo đồ án và bản demo các luồng nghiệp vụ chính.

Các sản phẩm trên là kết quả dự kiến cần hoàn thiện và nghiệm thu, không phải xác nhận rằng tất cả đã hoàn thành tại thời điểm lập kế hoạch.

## 2. REVIEW SRS VÀ WBS

### 2.1. SRS — Đặc tả yêu cầu phần mềm

SRS (Software Requirements Specification) mô tả các yêu cầu chức năng, phi chức năng và quy tắc nghiệp vụ mà hệ thống cần đáp ứng.

#### 2.1.1. Các tác nhân của hệ thống

- **Admin:** Quản lý người dùng, vai trò, quyền hạn và hoạt động vận hành của hệ thống.
- **AI:** Hỗ trợ hướng dẫn học tập, tạo hoặc cung cấp hoạt động luyện tập, phân tích kết quả và đưa ra phản hồi theo chức năng được tích hợp.
- **Mentor:** Hỗ trợ giải đáp thắc mắc, tham gia cộng đồng, theo dõi tiến độ người học được phân công và hỗ trợ khi người học cần sự can thiệp của con người.
- **Learner:** Thực hiện hoạt động học tập, luyện tập với AI, nhận phản hồi, theo dõi tiến độ và tham gia cộng đồng.

#### 2.1.2. Yêu cầu chức năng
- **FR-01 — Xác thực và phân quyền:** Hệ thống xác thực người dùng và kiểm soát quyền truy cập theo vai trò.
- **FR-02 — Học tập với AI:** Người học có thể tương tác với AI trong các hoạt động học tập được hỗ trợ.
- **FR-03 — Luyện tập và đánh giá:** Người học thực hiện bài tập hoặc thử thách và nhận phản hồi theo luồng xử lý của hệ thống.
- **FR-04 — Theo dõi tiến độ:** Hệ thống lưu trữ và hiển thị thông tin kết quả, tiến độ học tập.
- **FR-05 — Hỗ trợ từ Mentor:** Mentor giải đáp thắc mắc và hỗ trợ người học thuộc phạm vi được phân công.
- **FR-06 — Cộng đồng học tập:** Người dùng tham gia trao đổi, thảo luận theo quyền hạn được cấp.
- **FR-07 — Quản trị hệ thống:** Admin quản lý người dùng và các chức năng vận hành được hệ thống cung cấp.

#### 2.1.3. Yêu cầu phi chức năng

- **Bảo mật:** Các API nhạy cảm phải xác thực người dùng và kiểm tra quyền truy cập tại backend.
- **Quyền riêng tư:** Người dùng không được truy cập dữ liệu ngoài phạm vi được cấp phép.
- **Tính nhất quán:** Kết quả học tập và phản hồi phải được lưu trữ, truy xuất phù hợp với trạng thái xử lý thực tế.
- **Khả năng bảo trì:** Mã nguồn cần được tổ chức hợp lý để thuận tiện sửa lỗi và phát triển thêm.
- **Khả năng sử dụng:** Giao diện cần dễ hiểu, các chức năng được bố trí phù hợp với vai trò người dùng.

#### 2.1.4. Quy tắc nghiệp vụ

1. AI là tác nhân hỗ trợ học tập chính của Learner.
2. Mentor thực hiện chức năng hỗ trợ, không mặc định là người giảng dạy hoặc đánh giá chính.
3. Mentor chỉ được truy cập dữ liệu người học thuộc phạm vi được phân công.
4. Learner chỉ được truy cập dữ liệu học tập của chính mình, trừ những dữ liệu được chia sẻ hợp lệ.
5. Admin quản lý hệ thống theo quyền hạn được quy định.
6. Mọi thay đổi quyền truy cập phải được thực thi tại backend, không chỉ dựa vào giao diện.

### 2.2. WBS — Cấu trúc phân rã công việc

WBS (Work Breakdown Structure) phân chia dự án thành các nhóm công việc nhỏ nhằm quản lý phạm vi, tiến độ và kết quả thực hiện.

**Nhóm công việc 1: Khảo sát và phân tích yêu cầu**
- Khảo sát bài toán và hiện trạng hệ thống.
- Xác định mục tiêu, phạm vi và các tác nhân.
- Xây dựng và rà soát SRS.
**Nhóm công việc 2: Phân tích và thiết kế**
- Rà soát kiến trúc frontend và backend.
- Rà soát thiết kế cơ sở dữ liệu và API.
- Xác định quy tắc nghiệp vụ và phân quyền.

**Nhóm công việc 3: Phát triển chức năng học tập AI**
- Rà soát luồng học tập và luyện tập hiện có.
- Hoàn thiện tích hợp AI và phản hồi.
- Hoàn thiện lưu trữ kết quả và theo dõi tiến độ.

**Nhóm công việc 4: Phát triển chức năng hỗ trợ học tập**
- Điều chỉnh chức năng Mentor theo vai trò hỗ trợ.
- Hoàn thiện các chức năng cộng đồng và giải đáp thắc mắc.
- Kiểm tra phạm vi truy cập dữ liệu người học.

**Nhóm công việc 5: Phát triển chức năng quản trị**
- Rà soát quản lý tài khoản và vai trò.
- Hoàn thiện chức năng quản lý hệ thống theo phạm vi.

**Nhóm công việc 6: Tích hợp và kiểm thử**
- Kiểm thử chức năng và API.
- Kiểm thử quyền truy cập và bảo mật.
- Kiểm thử tích hợp frontend, backend và cơ sở dữ liệu.
- Sửa lỗi và kiểm thử hồi quy.

**Nhóm công việc 7: Hoàn thiện và bàn giao**
- Hoàn thiện tài liệu kỹ thuật.
- Viết hướng dẫn cài đặt và sử dụng.
- Chuẩn bị báo cáo, demo và nghiệm thu.

## 3. REVIEW WORKSPACE (GIT)

### 3.1. Repository dự án

Đường dẫn repository: (https://github.com/thbao1008/AESP)

Repository được sử dụng để quản lý mã nguồn, theo dõi thay đổi và hỗ trợ quá trình phát triển, kiểm thử hệ thống AESP.

### 3.2. Nội dung cần rà soát

- Cấu trúc mã nguồn frontend, backend và các dịch vụ.
- Cấu trúc cơ sở dữ liệu, schema và các migration.
- Cấu hình môi trường chạy ứng dụng.
- Các chức năng đã triển khai và các chức năng đang cần hoàn thiện.
- Các bài kiểm thử hiện có và kết quả kiểm thử.
- Lịch sử thay đổi mã nguồn và cách tổ chức công việc trên Git.

### 3.3. Kế hoạch quản lý mã nguồn

- Sử dụng Git để theo dõi các thay đổi.
- Đặt tên commit mô tả rõ nội dung thay đổi.
- Kiểm tra diff trước khi tích hợp thay đổi.
- Không đưa thông tin bí mật như mật khẩu, token hoặc khóa API vào repository.
- Kiểm thử các chức năng bị ảnh hưởng sau mỗi thay đổi lớn.
- Duy trì tài liệu hướng dẫn cài đặt và chạy dự án.

### Kết luận

Trong giai đoạn thực hiện đồ án, AESP tập trung vào việc rà soát yêu cầu, xác định phạm vi và hoàn thiện các luồng nghiệp vụ theo mô hình AI hỗ trợ học tập là chính, Mentor hỗ trợ người học và Admin quản lý hệ thống. Các bước tiếp theo là hoàn thiện đặc tả yêu cầu, lập kế hoạch thực hiện chi tiết, kiểm chứng mã nguồn hiện tại và kiểm thử tích hợp để đảm bảo sản phẩm đáp ứng phạm vi đã thống nhất với giảng viên.
