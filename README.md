# HostelHub 🏠
### Smart Hostel & PG Management Portal

HostelHub is a web-based hostel and paying-guest management portal designed to centralize hostel information, resident services, maintenance requests, billing, and administrative operations in one place.

The application uses WordPress as its content management system and extends its functionality through a custom PHP plugin. It supports multiple hostels, role-specific dashboards, room and bed allocation, payment history, PDF receipts, complaints, and leave requests.

## ✨ Features

### 🌐 Public Website
- Hostel information and property listings
- Hostel notices, rules, and FAQs
- Multi-hostel support for Youthville SBR 1 and SBR 2

### 👤 Resident Portal
- Resident login and personalized dashboard
- Profile and room allocation information
- Billing and payment history
- Razorpay Test Mode payment workflow
- PDF receipt generation and access
- Maintenance complaint submission
- Leave request submission

### 🛠️ Staff Portal
- Staff login and dedicated dashboard
- View assigned maintenance work
- Track assigned complaints

### 🔐 Administration
- Manage hostels, rooms, beds, and resident records
- Assign complaints to maintenance staff
- Update complaint status
- Trigger resident email notifications when complaints are resolved

## 🧰 Technology Stack

| Component | Technology |
|---|---|
| CMS | WordPress |
| Backend | PHP |
| Database | MariaDB / MySQL |
| Frontend | HTML, CSS, JavaScript |
| Client-side interactions | jQuery and AJAX where implemented |
| Payment integration | Razorpay Test Mode |
| PDF generation | Dompdf |
| Email | WordPress `wp_mail()` with WP Mail SMTP configuration |
| Web server | Apache |
| Hosting | AWS EC2 |
| Server environment | Ubuntu 24.04, PHP 8.3, MariaDB 10.11 |
| Local development | Windows, XAMPP |

## 🏗️ Architecture

The application follows a WordPress-based web architecture.

1. The browser sends requests to the Apache web server.
2. WordPress loads the active theme and the custom HostelHub plugin.
3. The plugin handles hostel management workflows and application-specific logic using PHP.
4. MariaDB/MySQL stores the relevant application records.
5. JavaScript, jQuery, and AJAX support interactive interfaces where implemented.
6. Configured payment, PDF generation, and email components support their respective workflows.

## 🗂️ Main Modules

- **Hostel Management:** Hostel, room, bed, and resident administration.
- **Resident Management:** Profile, room allocation, and resident dashboard.
- **Billing and Payments:** Billing information, transaction history, and test-mode payment workflow.
- **Receipt Generation:** PDF receipts accessible through the application.
- **Complaint Management:** Complaint submission, staff assignment, and resolution tracking.
- **Leave Management:** Resident leave request submission.
- **Content Management:** Public hostel information, notices, and rules.
- **Notifications:** Configured email notification when a complaint is resolved.

## 🚀 Deployment

The project was deployed on an Ubuntu-based AWS EC2 instance using Apache, PHP, MariaDB, and WordPress.

For local development, a Windows environment with XAMPP and MariaDB/MySQL was used.

Refer to the project documentation and the actual deployment configuration before reproducing the environment.

## ⚙️ Local Setup

### Prerequisites

- XAMPP or an equivalent PHP/MySQL environment
- A compatible WordPress installation
- PHP and database versions compatible with the project
- The HostelHub plugin source code
- Any required plugin dependencies, including Dompdf if used by the application

### Installation

1. Install and start Apache and MySQL through XAMPP.
2. Create a local database for WordPress.
3. Install WordPress in the local web server directory.
4. Copy the HostelHub plugin into `wp-content/plugins/hostelhub/`.
5. Configure WordPress using your local database credentials.
6. Activate the HostelHub plugin from the WordPress administration dashboard.
7. Configure the required pages, shortcodes, and application settings according to the implementation.
8. Configure email and Razorpay Test Mode credentials using local, non-production settings.
9. Test the resident, staff, and administrator workflows.

**Note:** These are general setup steps. Exact database import instructions, page names, shortcode names, and configuration values must be documented from the final source code.

## 🧪 Testing

The project report records successful manual checks of the following workflows:

- Public hostel information and notices
- Resident login, dashboard, profile, and room allocation
- Billing, test payment, and PDF receipt access
- Complaint and leave request submission
- Staff login and assigned-work view
- Administrative hostel, room, bed, and resident management
- Complaint assignment, resolution, and resident email notification
- Logout, redirects, and mobile usability

These results represent manual demonstration checks, not an automated test suite or a formal security audit.

## 🔒 Security Considerations

- Use role-specific access checks for resident, staff, and administrator workflows.
- Protect AJAX actions with appropriate nonce validation and authorization checks.
- Never commit credentials, API secrets, or production configuration files.
- Use test payment credentials for development and testing.
- Configure HTTPS before handling real resident or payment data.
- Review input validation, access control, file access, payment verification, and session handling before production use.
- Keep database exports free of unnecessary personal information.

## 🔮 Future Enhancements

- Automated regression tests for core workflows
- Improved audit logging and monitoring
- Automated backups and tested recovery procedures
- Stronger security review and production HTTPS configuration
- Further improvements to operational reliability and deployment

## 📚 Documentation

The `docs/` directory can contain the project report, architecture diagram, interface screenshots, and setup documentation.

## 👥 Team

Developed collaboratively by:

- **Dhruv Agarwal** — Core implementation and integration
- **Aishwarya Gilhotra** — User-facing workflow review, validation, testing, and documentation support
- **Rishi Chaurasia** — Administrative and database workflow review, testing, and evidence collection

**Institution:** Symbiosis Institute of Computer Studies and Research (SICSR), Pune  
**Academic Year:** 2026

## 📄 License

Add a license after confirming that the project source code can be publicly distributed and that all contributors agree to its terms.
