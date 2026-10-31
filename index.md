layout: default
title: [Farisa Rahman] | Portfolio
---
<script>
  (async function() {
    // Check if the user has already logged in during this session
    if (sessionStorage.getItem("portfolio_auth") === "true") return;

    // Helper function to scramble the user's input using SHA-256
    async function hashPassword(string) {
      const utf8 = new TextEncoder().encode(string);
      const hashBuffer = await crypto.subtle.digest('SHA-256', utf8);
      const hashArray = Array.from(new Uint8Array(hashBuffer));
      return hashArray.map(b => b.toString(16).padStart(2, '0')).join('');
    }

    // paste your scrambled letters/numbers hash below inside the quotes
    const targetHash = "MywD2fB8wDr84jH"; 

    // Prompt the user for the password
    let authenticated = false;
    let input = prompt("This portfolio is password protected. Please enter the password to view:");

    if (input !== null) {
      const inputHash = await hashPassword(input);
      if (inputHash === targetHash) {
        authenticated = true;
        sessionStorage.setItem("portfolio_auth", "true");
      }
    }

    if (!authenticated) {
      alert("Incorrect password. Access denied.");
      document.write('<h2 style="font-family:sans-serif; text-align:center; margin-top:50px;">Access Denied: Invalid Password</h2>');
      window.stop();
    }
  })();
</script>

--

# Hello, I'm [Farisa]
### Recent Graduate

Welcome to my portfolio! I have worked/interned/volunteered in multiple industries and have developed a multitude of transferable skills. Continue to explore my page!

---

## 🛠️ Skills & Tooling

* **Technical:** R, Python, HTML, SQL, VBA Macros(In Progress)
* **Tools:** Asana, Notion, Canva, Google Sheets, Excel
* **Core Competencies:** Project Management, Research, Marketing, Market Research, Writing, Database Design, Resource Allocation

---

## 📁 Key Case Studies

### 1. [Summer Streets Tabling 2025 - CLIP (Climate Tech Startup]
* **Role:** Lead Planner
* **Timeline:** 1 Month | **Budget:** $30

#### **The Challenge**
[Need to create engaging activities that will also introduce customers to our products and collect contact information for promotional mail. Limited budget to buy additional materials. No wifi to use our company Ipad.]

#### **My Approach & Strategy**
* **Scope & Planning:** Build a detailed document linking QR codes, posters, and checklist to be used before every event. Designed an activity where attendees can enter their email and have the chance to win a bike tour. Find cheap ways to incentivize people to come to the table.
* **Task Delegation:** Delegate tasks such as printing QR cutouts linking to company website and designing a poster for the bike raffle. 
* **Testing:** Improved quality of activities based on user friendliness in the planning stages. Made updates to activity strategy after the first event so that people could provide email addresses without participating in a quiz activity. Removed marketing materials that were rejected by cofounder.
* **Execution:** Took notes on tech questions that customers had and passed it to other members of the team Checklist refreshed before every event, email addresses were transferred to CRM after each event, and handwritten email addresses were uploaded.

#### **The Result**
* **Impact:** All activities and market research notes can be used for the following year. 
* **Metric:** Newsletter sent to 77+ new potential customers.

---

### 2. [Project Title, e.g., Process Optimization & Tool Implementation]
* **Role:** Scrum Master / Project Manager
* **Timeline:** 3 Months | **Budget:** Internal Resources

#### **The Challenge**
[ffff ]

#### **My Approach & Strategy**
* **Workflow Design:** Audited current operational gaps and mapped a custom, streamlined workflow into Asana.
* **Change Management:** Conducted onboarding workshops and created simple documentation playbooks for a smooth team transition.

#### **The Result**
* **Impact:** Successfully onboarded 35 team members onto the new platform.
* **Metric:** Increased on-time project delivery from 65% to **92% within the first 60 days**.

---

## Education
* **Bachelor of Arts in Economics, Minor in Data Science** – [New York University ]

---

## 📨 Let's Connect

* **LinkedIn:** [://linkedin/com](https://linkedin.com/farisa-rahman)
