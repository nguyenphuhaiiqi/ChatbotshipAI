# 📊 Database Schema (Lược đồ Cơ sở dữ liệu)

Đây là thiết kế database cho Nền Tảng Giao Đồ Ăn Thông Minh.

## 1. Bảng cho Smart Shipper (Feature 1)
* `shipper_customer_history`
    * `id` (Khóa chính)
    * `customer_id`
    * `shipper_id`
    * `last_order_date`
    * `total_orders`
    * `rating`
* `order_assignment_preferences`
    * `id` (Khóa chính)
    * `customer_id`
    * `prefer_known_shipper` (Boolean)
    * `preferred_shipper_id`

## 2. Bảng cho Voice & Avatar (Feature 2 & 3)
* `voice_sessions`
    * `id` (Khóa chính)
    * `customer_phone`
    * `session_id_elevenlabs`
    * `session_id_heygen`
    * `is_active` (Boolean)
* `customer_preferences`
    * `id` (Khóa chính)
    * `customer_id`
    * `voice_enabled` (Boolean)
    * `preferred_voice_id`
* `emotion_context_mapping`
    * `id` (Khóa chính)
    * `trigger_keyword`
    * `emotion_name` (ví dụ: "Friendly_smile")
    * `priority` (Integer)

## 3. Bảng cho Rating System (Feature 4)
* `ratings`
    * `id` (Khóa chính)
    * `ratee_type` (Quán / Tài xế / Khách)
    * `ratee_id`
    * `rater_type`
    * `rater_id`
    * `rating_score` (1-5)
    * `comment`
    * `is_public` (Boolean)
    * 
