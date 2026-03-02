# Small Company Enterprise Network Design

## Project Overview

This project presents the design and simulation of an enterprise network for a small company operating across two branches:
* Ho Chi Minh City (HCM)
* Da Nang (DN)

The objective of this project is to build a structured, segmented, and scalable network infrastructure using Cisco technologies and standard enterprise design principles.
The network was implemented and tested using Cisco Packet Tracer.
---

## Network Architecture

Each branch includes:
* 1 Router (WAN connectivity)
* 1 Layer 3 Switch (Inter-VLAN routing)
* Department-based VLAN segmentation
* Structured IP addressing
* IPS for basic security monitoring

The design follows a simplified hierarchical model:
* Distribution Layer – Layer 3 Switch
* Access Layer – End-user devices
* Edge/WAN Layer – Router

This structure allows logical segmentation, simplified routing, and easier scalability.


## VLAN Segmentation

| VLAN | Department      |
| ---- | --------------- |
| 10   | Management      |
| 20   | IT              |
| 30   | Accounting      |
| 40   | Sales           |
| 99   | Management VLAN |

Each VLAN is assigned a dedicated subnet and default gateway configured on the Layer 3 switch.
Benefits:
* Reduced broadcast domain
* Logical traffic separation
* Improved manageability
* Better scalability

## Inter-VLAN Routing
Inter-VLAN routing is implemented directly on the Layer 3 switches to enable communication between departments while maintaining logical separation.

##  WAN Connectivity
The two branches are connected using point-to-point WAN configuration with static routing to ensure stable inter-branch communication.

---

## IP Addressing Plan
The project includes a structured IP allocation strategy:
* Dedicated subnet per VLAN
* Standard gateway allocation (.1)
* Separate WAN subnet
* Private IP addressing scheme

Detailed documentation is available in:

IP_Addressing_Plan.xlsx

## Security Implementation
* Basic IPS configuration
* VLAN isolation
* Separation of management network

The objective is to apply security thinking during the design phase.

## Repository Structure

├── network-design.pkt
├── IP_Addressing_Plan.xlsx
└── configs/
    ├── RT-HCM_config.txt
    ├── RT-DN_config.txt
    ├── SW-Layer3-HCM_config.txt
    ├── SW-Layer3-DN_config.txt
    └── IPS_config.txt

All device configurations are separated to reflect real-world deployment practices.

## Technologies Used
* Cisco Packet Tracer
* VLAN
* Inter-VLAN Routing
* Static Routing
* Layer 3 Switching
* IP Subnetting
* Basic Network Security (IPS)

## Skills Demonstrated
* Enterprise network design
* IP subnet planning
* Cisco CLI configuration
* Multi-site connectivity
* Network segmentation
* Structured documentation


## Future Improvements
* OSPF dynamic routing
* ACL implementation
* NAT configuration
* Firewall integration
* Redundancy (HSRP / STP tuning)

## Author
Nguyen Ho Yen Oanh
Network Engineering Student
Ho Chi Minh City, Vietnam

================================================================================================
# Thiết Kế Hệ Thống Mạng Doanh Nghiệp Nhỏ
## Tổng quan dự án
Dự án này mô phỏng thiết kế hệ thống mạng cho một doanh nghiệp nhỏ có hai chi nhánh:
* Hồ Chí Minh
* Đà Nẵng

Mục tiêu là xây dựng một hệ thống mạng có cấu trúc rõ ràng, phân chia hợp lý và có khả năng mở rộng, dựa trên mô hình triển khai thực tế trong doanh nghiệp.
Hệ thống được triển khai và kiểm thử bằng Cisco Packet Tracer.

## Kiến trúc mạng
Mỗi chi nhánh bao gồm:
* 1 Router kết nối WAN
* 1 Switch Layer 3 thực hiện định tuyến giữa các VLAN
* Phân chia VLAN theo phòng ban
* Kế hoạch cấp phát IP rõ ràng
* Thiết bị IPS để giám sát an ninh cơ bản

Thiết kế dựa trên mô hình phân tầng đơn giản, phù hợp với doanh nghiệp vừa và nhỏ.

## Phân chia VLAN

* VLAN 10 – Ban quản lý
* VLAN 20 – Phòng IT
* VLAN 30 – Phòng Kế toán
* VLAN 40 – Phòng Kinh doanh
* VLAN 99 – VLAN quản trị thiết bị
Mỗi VLAN được cấp một subnet riêng và gateway mặc định trên Switch Layer 3.

Lợi ích:
* Giảm broadcast
* Phân tách lưu lượng theo phòng ban
* Dễ quản lý và mở rộng

## Định tuyến giữa VLAN
Định tuyến giữa các VLAN được thực hiện trên Switch Layer 3, giúp các phòng ban có thể giao tiếp với nhau khi cần thiết nhưng vẫn đảm bảo phân tách mạng.

##  Kết nối giữa hai chi nhánh
Hai chi nhánh được kết nối qua WAN point-to-point và sử dụng static routing để đảm bảo liên lạc ổn định giữa hai site.


## Kế hoạch cấp phát IP
Dự án có xây dựng bảng phân bổ IP chi tiết:
* Mỗi VLAN một subnet riêng
* Gateway chuẩn hóa (.1)
* Subnet riêng cho WAN
* Sử dụng IP private

Chi tiết trong file:
_IP_Addressing_Plan.xlsx_

## Triển khai bảo mật
* Cấu hình IPS cơ bản
* Cô lập VLAN
* Tách riêng mạng quản trị
Mục tiêu là hình thành tư duy bảo mật ngay từ giai đoạn thiết kế.


## Công nghệ sử dụng
* Cisco Packet Tracer
* VLAN
* Inter-VLAN Routing
* Static Routing
* Layer 3 Switching
* IP Subnetting
* IPS cơ bản

## Kỹ năng thể hiện
* Thiết kế mạng doanh nghiệp
* Lập kế hoạch chia subnet
* Cấu hình thiết bị Cisco bằng CLI
* Kết nối nhiều chi nhánh
* Phân tách mạng logic
* Tổ chức tài liệu cấu hình rõ ràng
