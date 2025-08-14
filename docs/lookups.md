| Lookup Id | Value |
|-|-|
| <span id="application">APPLICATION</span> | 1 |
| <span id="brand">BRAND</span> | 2 |
| <span id="department">DEPARTMENT</span> | 3 |
| <span id="survey_status">SURVEY_STATUS</span> | 4 |
| <span id="channel_setup">CHANNEL_SETUP</span> | 5 |
| <span id="user_role">USER_ROLE</span> | 6 |
| <span id="channel_sub_setup">CHANNEL_SUB_SETUP</span> | 7 |
| <span id="survey_status_header">SURVEY_STATUS_HEADER</span> | 8 |
| <span id="survey_interactive_type">SURVEY_INTERACTIVE_TYPE</span> | 9 |
| <span id="question_master">QUESTION_MASTER</span> | 10 |
| <span id="answer_master">ANSWER_MASTER</span> | 11 |
| <span id="survey_response_header_status">SURVEY_RESPONSE_HEADER_STATUS</span> | 16 |
| <span id="template_type">TEMPLATE_TYPE</span> | 17 |
| <span id="broadcast_status">BROADCAST_STATUS</span> | 20 |
| <span id="agent_status">AGENT_STATUS</span> | 21 |
| <span id="priority">PRIORITY</span> | 22 |
| <span id="impact">IMPACT</span> | 23 |
| <span id="category">CATEGORY</span> | 24 |
| <span id="subcategory">SUBCATEGORY</span> | 25 |
| <span id="customer_type">CUSTOMER_TYPE</span> | 27 |
| <span id="complaint_state">COMPLAINT_STATE</span> | 28 |
| <span id="activity_state">ACTIVITY_STATE</span> | 30 |
| <span id="message_type">MESSAGE_TYPE</span> | 37 |
| <span id="customer_industry_type">CUSTOMER_INDUSTRY_TYPE</span> | 39 |
| <span id="user_types">USER_TYPES</span> | 40 |
| <span id="file_instance_type">FILE_INSTANCE_TYPE</span> | 41 |
| <span id="notification_status">NOTIFICATION_STATUS</span> | 43 |
| <span id="notification_type">NOTIFICATION_TYPE</span> | 44 |
| <span id="file_sub_instance_type">FILE_SUB_INSTANCE_TYPE</span> | 42 |
| <span id="identification_type">IDENTIFICATION_TYPE</span> | 49 |
| <span id="title">TITLE</span> | 50 |
| <span id="nationality">NATIONALITY</span> | 51 |
| <span id="gender">GENDER</span> | 52 |
| <span id="occupation">OCCUPATION</span> | 53 |
| <span id="language">LANGUAGE</span> | 54 |
| <span id="contact_type">CONTACT_TYPE</span> | 55 |
| <span id="country">COUNTRY</span> | 56 |
| <span id="region">REGION</span> | 57 |
| <span id="city">CITY</span> | 58 |
| <span id="purchase_plan">PURCHASE_PLAN</span> | 59 |
| <span id="payment_mode">PAYMENT_MODE</span> | 60 |
| <span id="currency">CURRENCY</span> | 61 |
| <span id="phone_code">PHONE_CODE</span> | 62 |
| <span id="model">MODEL</span> | 63 |
| <span id="model_year">MODEL_YEAR</span> | 64 |
| <span id="vehicle_type">VEHICLE_TYPE</span> | 65 |
| <span id="business_area">BUSINESS_AREA</span> | 66 |
| <span id="access_type">ACCESS_TYPE</span> | 69 |
| <span id="lead_source">LEAD_SOURCE</span> | 70 |
| <span id="lead_sub_source">LEAD_SUB_SOURCE</span> | 71 |
| <span id="lead_stage">LEAD_STAGE</span> | 72 |
| <span id="lead_status">LEAD_STATUS</span> | 73 |
| <span id="lead_interest">LEAD_INTEREST</span> | 74 |
| <span id="lead_priority">LEAD_PRIORITY</span> | 75 |
| <span id="lead_label">LEAD_LABEL</span> | 76 |
| <span id="lead_follow_up">LEAD_FOLLOW_UP</span> | 77 |
| <span id="lead_monthly_income">LEAD_MONTHLY_INCOME</span> | 78 |
| <span id="lead_vehicle_type">LEAD_VEHICLE_TYPE</span> | 79 |
| <span id="lead_flag">LEAD_FLAG</span> | 80 |
| <span id="lead_batch_status">LEAD_BATCH_STATUS</span> | 81 |
| <span id="lead_action">LEAD_ACTION</span> | 83 |
| <span id="lead_sub_action">LEAD_SUB_ACTION</span> | 84 |
| <span id="lead_import_source">LEAD_IMPORT_SOURCE</span> | 85 |
| <span id="lead_follow_up_reason_type">LEAD_FOLLOW_UP_REASON_TYPE</span> | 86 |
| <span id="lead_follow_up_mode_type">LEAD_FOLLOW_UP_MODE_TYPE</span> | 87 |
| <span id="lead_attention">LEAD_ATTENTION</span> | 88 |
| <span id="lead_reason">LEAD_REASON</span> | 89 |
| <span id="lead_sub_reason">LEAD_SUB_REASON</span> | 90 |
| <span id="customer_region">CUSTOMER_REGION</span> | 100 |
| <span id="customer_city">CUSTOMER_CITY</span> | 101 |
| <span id="ou_type">OU_TYPE</span> | 102 |
| <span id="branch_type">BRANCH_TYPE</span> | 103 |
| <span id="yes_or_no">YES_OR_NO</span> | 104 |


<script>
document.addEventListener("DOMContentLoaded", function() {
    const hash = window.location.hash.substr(1);
    if(hash) {
        const el = document.getElementById(hash);
        if(el) {
            // Add blinking class
            el.classList.add("blink-anchor");
            // Scroll into view
            el.scrollIntoView({ behavior: "smooth", block: "center" });

            // After 2s, remove blink and add permanent highlight
            setTimeout(() => {
                el.classList.remove("blink-anchor");
                el.classList.add("highlight-anchor");
            }, 2000);
        }
    }
});
</script>


