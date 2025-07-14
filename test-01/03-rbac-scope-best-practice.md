### 1. **Question Title**  
Avoiding Over-Permissioning with Proper Scope in Azure RBAC

---

### 2. **New MCQ Scenario Statement**  
Ayesha is a cloud engineer at **SkyBridgeTech**, where each development team works on a different application hosted in Azure. These applications are isolated in separate **resource groups**, all under a shared **subscription**. The organization uses **Microsoft Entra Connect** to sync with on-premises Active Directory (AD DS), and team members often work across multiple apps.

Initially, Ayesha assigned roles at the **resource group level** for fine-grained access. However, to simplify management, she decides to remove those assignments and instead give each user the same role at the **subscription level** — thinking it would be more efficient.

She now wants to verify whether this change still supports the principle of least privilege while keeping access manageable.

Does Ayesha’s revised approach meet the goal?

---

### 3. **Answer Choices**  
(a) Yes, because assigning roles at the subscription level makes it easier to manage large groups of users  
(b) No, because assigning roles at the subscription level gives unnecessary access to unrelated resource groups  
(c) Yes, because role inheritance ensures correct access flows down to the resource groups  
(d) No, because Entra ID doesn't support subscription-level RBAC  

---

### ✅ 4. **Correct Answer:** (B)

---

### 💡 5. **Explanation**  
**Why (B) is correct:**  
By assigning roles at the **subscription level**, Ayesha ends up granting access to **all resource groups** under that subscription. This goes against the **principle of least privilege**, which aims to give users only the permissions they absolutely need. In this case, users may gain access to apps they aren’t responsible for — which introduces both security and governance risks.

**Why the other options are incorrect:**  
- **(A)** is tempting from a management point of view, but it’s risky. Easier does not mean safer — it overexposes users to resources they shouldn’t access.  
- **(C)** is technically true that permissions flow down, but that’s the *problem* here — not a benefit. It grants too much access.  
- **(D)** is simply incorrect — Microsoft Entra (formerly Azure AD) absolutely supports RBAC at the subscription level.

---

### 💬 6. **Reflective Quote from Jamalu (Learner’s Inner Guide)**  
________________________________________  
"Permission without precision creates chaos in the cloud."  
— Jamalu  
— Siraat AI Academy  
________________________________________

---

### 🔗 Additional Learning Resources  
1. **MS Learn URL:** [Role-based access control (RBAC) in Azure](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview)  
2. **YouTube video for the question:** []
