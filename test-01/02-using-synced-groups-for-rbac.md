### 1. **Question Title**  
Using Synced Security Groups for RBAC in Azure

---

### 2. **New MCQ Scenario Statement**  
Omar works at **CloudCore Labs**, where the organization manages several internal tools hosted in Azure. Each tool lives in its own resource group, and the entire Azure subscription is connected to their on-premises Active Directory via Microsoft Entra Connect.

To simplify how users gain access to the tools, Omar wants to avoid assigning roles to users one-by-one. Instead, he uses their existing AD DS security groups — which are already structured by department — and assigns Azure roles to these groups at the resource group level. Members of each group need access to manage the resources relevant to their department.

Omar wants to know if this method effectively grants access to Azure resources while keeping administration streamlined.

Does this approach meet the goal?

---

### 3. **Answer Choices**  
(a) No, because AD DS groups can’t be used for Azure role assignments  
(b) Yes, because AD DS groups synced via Entra Connect can be used in role assignments  
(c) No, because you must use Microsoft Entra dynamic groups for RBAC  
(d) Yes, but only if group-based access is assigned at the subscription level  

---

### ✅ 4. **Correct Answer:** (B)

---

### 💡 5. **Explanation**  
**Why (B) is correct:**  
Since Omar’s organization has **Microsoft Entra Connect** syncing their **on-premises AD DS**, the **security groups from AD DS become available in Entra ID** (formerly Azure AD). This means those groups **can be used for role assignments** in Azure. It's an efficient way to centralize and automate access control without manually handling every user.

**Why the other options are incorrect:**  
- **(A)** is wrong because synced AD DS groups *can* be used in Azure RBAC — assuming Entra Connect is configured, as in this scenario.  
- **(C)** misunderstands the need: dynamic groups are useful for automation but are not a requirement for assigning roles.  
- **(D)** confuses scope — role assignments don't *have* to be made at the subscription level; **resource group-level** assignments are common and align with least-privilege principles.

---

### 💬 6. **Reflective Quote from Jamalu (Learner’s Inner Guide)**  
________________________________________  
"The simpler your system of access, the stronger your foundation of trust."  
— Jamalu  
— Siraat AI Academy  
________________________________________

---

### 🔗 Additional Learning Resources  
1. **MS Learn URL:** [How to manage Microsoft Entra groups](https://learn.microsoft.com/en-us/entra/fundamentals/how-to-manage-groups)  
2. **YouTube video for the question:** []
