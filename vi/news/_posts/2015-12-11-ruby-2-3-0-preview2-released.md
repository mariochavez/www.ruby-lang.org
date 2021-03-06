---
layout: news_post
title: "Ruby 2.3.0-preview2 Released"
author: "naruse"
translator: "Trung Lê"
date: 2015-12-11 14:00:00 +0000
lang: vi
---

Chúng tôi hân hạnh công bố ấn bản Ruby 2.3.0-preview2.

Ruby 2.3.0-preview2 là phiên bản thử nghiệm thứ hai của Ruby 2.3.0.
Giới thiệu cùng với phiên bản này bao gồm các cải tiến sau:

[Frozen String Literal
Pragma](https://bugs.ruby-lang.org/issues/11473) được giới thiệu. Trên
Ruby 2.1, "str".freeze được tối ưu hoá để giảm số lượng đối tượng được
tạo ra. Ruby 2.3 cho phép đóng băng tất cả chuỗi ký tự trong các
file mã nguồn thông qua một magic comment và một cờ của command line.
Ngoài ra người dùng còn có thể biết được vị trí đổi tượng được tạo
khi gặp phải lỗi "can't modify frozen String" thông qua cờ `--enable-frozen-string-literal-debug`.

[Safe navigation operator](https://bugs.ruby-lang.org/issues/11537)
([hay còn gọi là lonely operator](https://instagram.com/p/-M9l6mRPLR/)) `&.`,
chức năng này đã hiện diện trong C#, Groovy, và Swift. Cú pháp này
được giới thiệu để làm giảm thiểu sự phiền toái khi xử lý `nil`, xem ví dụ:
`obj&.foo`. `Array#dig` và `Hash#dig` cũng mới được bổ sung vào thư viện.

[Giới thiệu did_you_mean gem](https://bugs.ruby-lang.org/issues/11252).
did_you_mean gem hiển thị những gợi ý trong trường hợp gặp lỗi `NameError`
hay `NoMethodError` giúp cho việc debug dễ dàng hơn.

[RubyVM::InstructionSequence#to_binary and .load_from_binary](https://bugs.ruby-lang.org/issues/11788)
là các tính năng thử nghiệm được giới thiệu trong phiên bản này. Với các chức năng này
chúng ta có thể tạo ra một hệ thống biên dịch trước ISeq (bytecode).

Ruby 2.3 còn kèm theo các cải tiến về phần hiệu chỉnh công suất.
Ví dụ, [tối ưu hoá Proc#call](https://bugs.ruby-lang.org/issues/11569),
[xem xét lại phần cấu trúc dữ liệu hàm nhập](https://bugs.ruby-lang.org/issues/11278),
[giới thiệu kiểu cấu trúc dữ liệu bảng mới](https://bugs.ruby-lang.org/issues/11420),
hiệu chỉnh ở tầng mã máy cho việc gán phần tử và hàm gọi mã, 
và nhiều tối ưu khác.

Hãy thử sử dụng Ruby 2.3.0-preview2, và cho chúng tôi biết trải nghiệm của bạn.

## Các thay đổi đáng chú ý so với 2.2

Xem [NEWS](https://github.com/ruby/ruby/blob/v2_3_0_preview2/NEWS)
và [ChangeLog](https://github.com/ruby/ruby/blob/v2_3_0_preview2/ChangeLog)
để biết thêm chi tiết.

Các thay đổi: [1097 files bị thay đổi, 97466 thêm vào(+), 58685 loại bỏ(-)](https://github.com/ruby/ruby/compare/v2_2_0...v2_3_0_preview2) kể từ Ruby 2.2.0!

## Download

* <https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.0-preview2.tar.bz2>

  * SIZE:   14126752 bytes
  * SHA1:   7e717ef7a0a1523ad696b5fe693f7f7a613a3810
  * SHA256: e9b0464e50b2e5c31546e6b8ca8cad71fe2d2146ccf88b7419bbe9626af741cb
  * SHA512: e397f321d4338edba8d005d871408775f03d975da90c8abcfdb457a1bc7e6c87efe58c53b2c3bc122e9f58f619767b271bcc8d5d9663ed4b4288c60556e8d288

* <https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.0-preview2.tar.gz>

  * SIZE:   17623519 bytes
  * SHA1:   2deaf3ccbbfc5e08d3d840a4f1c33ff5f62f931d
  * SHA256: cb1c745bda33ba9e812b48c87852571ef6486f985c5e6ff4508a137d1c9734a3
  * SHA512: 83022f99775eb139beec281d59029dcc7c59de1e313182685b0a785334ac53d0c445212460d00d065169b922949263f30a1f981e19fc6e59814e79e6e53ae8e0

* <https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.0-preview2.tar.xz>

  * SIZE:   11249780 bytes
  * SHA1:   e1dfca06cd3c2cf6456a7feb0b1cd0752bde1a3b
  * SHA256: 7c3119268af87c137f415301b299281762453ad78f86e35562be014dabd67b11
  * SHA512: ab3376145d95a2188e6345984f0e5592c8d33515d7046a2ab2565dc418fa2306cdcf797aae9494d4d10446ada54ba638d8a8ad2d4b7510544d7eaea3de4faa87

* <https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.0-preview2.zip>

  * SIZE:   19841531 bytes
  * SHA1:   db7fa5291d90e0a9c6f75c0cd068bc54050520d6
  * SHA256: 90d036fd1ec40aa8f5493821ac162bf69f505c5977db54afe53b8bf689d79b9d
  * SHA512: 05784df420018aaae7d09d41e872df708e861cacc74dc8ee97a9e3ac7458cb12b937523ad6def34d5ae2890a0cf037a8d61e365beb88d28acd84879b9391ad65

## Chú thích

Xin xem lịch ấn bản và các thông tin khác tại

[ReleaseEngineering23](https://bugs.ruby-lang.org/projects/ruby-trunk/wiki/ReleaseEngineering23)
