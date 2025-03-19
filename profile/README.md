# 💊 약속시간

## 💡 서비스 개요
> **[카카오테크 부트캠프 해커톤]** - LLM 기반 복약 관리 AI 서비스    

**약속시간**은 사용자(고령자)의 약물 복용을 안전하고 효과적으로 관리하는 맞춤형 AI 서비스입니다.

## 👥 팀원 소개
<table>
  <tbody>
    <tr>
      <td align="center"><img src="https://avatars.githubusercontent.com/u/141610719?v=4" width="120px;" alt=""/><br /><sub><b>AI <a href="https://github.com/haebo9">(haebo.seo)</a></b></sub><br /></td>
      <td align="center"><img src="https://avatars.githubusercontent.com/u/195836355?v=4" width="120px;" alt=""/><br /><sub><b>👑 AI <a href="https://github.com/r0mmmy">(romi.han)</a></b></sub><br /></td>
      <td align="center"><img src="https://avatars.githubusercontent.com/u/80756039?v=4" width="120px;" alt=""/><br /><sub><b>AI <a href="https://github.com/leejiyeonnn">(jenna.lee)</a></b></sub><br /></td>
     <tr/>
      <td align="center"><img src="https://avatars.githubusercontent.com/u/97009289?v=4" width="120px;" alt=""/><br /><sub><b>Cloud <a href="https://github.com/hdh985">(kevin.kim)</a></b></sub><br /></td>
      <td align="center"><img src="https://avatars.githubusercontent.com/u/87990439?v=4" width="120px;" alt=""/><br /><sub><b>BE <a href="https://github.com/zzeon9">(daisy.lee)</a></b></sub><br /></td>
      <td align="center"><img src="https://avatars.githubusercontent.com/u/81545875?v=4" width="120px;" alt=""/><br /><sub><b>FE <a href="https://github.com/chulsu0012">(zoe.hong)</a></b></sub><br /></td>
    </tr>
  </tbody>
</table>

## **🚀 주요 기능**  
✅ **AI 기반 복약 알림** - 사용자의 복약 일정을 자동으로 생성하고 알람을 제공합니다.  
✅ **음성 인식** - 사용자 음성을 분석하여 복약 기록을 자동으로 저장합니다.  
✅ **데이터 분석** - 복약 패턴을 분석하여 리포트를 생성하고 건강 관리에 도움을 줍니다.  
✅ **사용자 맞춤형 UI** - 고령자도 쉽게 사용할 수 있도록 직관적인 UX/UI 설계  

---

## **🛠 기술 스택**  
### **📌 Backend**
- **FastAPI** - 경량 REST API 서버
- **Spring Boot** - 핵심 서비스 로직 구현  
- **PostgreSQL** - RDS 기반 데이터 저장  

### **📌 Frontend**
- **React.js (Next.js)** - 사용자 친화적 웹 인터페이스  
- **TypeScript** - 안정적인 코드 유지보수  
- **TailwindCSS** - UI 디자인  

### **📌 AI / NLP**
- **OpenAI GPT / LangChain** - 복약 일정 생성 및 음성 인식  
- **Whisper API** - 음성 데이터를 텍스트로 변환  

### **📌 Cloud & DevOps**
- **AWS (EC2, RDS, S3, CloudFront, IAM, WAF, Auto Scaling)** - 인프라 구성  
- **Terraform** - 클라우드 자동화  
- **GitHub Actions** - CI/CD 자동 배포  

---

## **📡 아키텍처 구조**
### **🔹 전체 클라우드 아키텍처**
![Architecture](https://github.com/.github/profile/ProjectArchitecture.png)  

1️⃣ **사용자 → Route53 & CloudFront**  
2️⃣ **ALB (Application Load Balancer) → Auto Scaling (EC2)**  
3️⃣ **FastAPI / Spring Boot 서비스**  
4️⃣ **RDS (PostgreSQL) 데이터베이스**  
5️⃣ **S3 (정적 파일 저장) 및 CloudFront (CDN)**  

---

## **⚡ 프로젝트 실행 방법**
### **1️⃣ 로컬 환경 실행**
```bash
# Backend 실행
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
