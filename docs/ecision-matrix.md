# FitFlow Technology Decision Matrix

## IT3060 – Human Computer Interaction
### Lab Exercise 05 – Activity 3

---

## 1. Introduction

This document presents the weighted technology decision matrix used to
select the most suitable technology stack for the FitFlow redesign.

The evaluation consolidates the frontend, backend, database, and
authentication comparisons completed in Activities 1 and 2.

Each technology is evaluated against criteria relevant to FitFlow,
including performance, scalability, development speed, security,
cost, AI/ML support, maintainability, code reusability, real-time
capabilities, and web compatibility.

---

## 2. Scoring Method

Each technology is rated using a five-point scale:

| Score | Meaning |
|---|---|
| 1 | Very Poor |
| 2 | Poor |
| 3 | Average |
| 4 | Good |
| 5 | Excellent |

The weighted score is calculated using:

**Weighted Score = (Technology Score / 5) × Criterion Weight**

The final total is presented out of 100.

---

# 3. Frontend Technology Decision Matrix

## 3.1 Criteria and Weights

| Criterion | Weight |
|---|---:|
| Performance | 15% |
| Development Speed | 15% |
| Code Reusability | 15% |
| Security | 10% |
| Cost | 10% |
| AI/ML Integration | 10% |
| Maintainability | 10% |
| Web Compatibility | 10% |
| Ecosystem Support | 5% |
| **Total** | **100%** |

## 3.2 Frontend Scores

| Technology | Performance | Development Speed | Code Reuse | Security | Cost | AI/ML | Maintainability | Web | Ecosystem | Weighted Total |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Flutter | 5 | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | **91/100** |
| **React Native** | **4** | **5** | **5** | **4** | **5** | **5** | **5** | **4** | **5** | **93/100** |
| Kotlin Multiplatform | 5 | 3 | 4 | 5 | 3 | 4 | 3 | 3 | 3 | **75/100** |
| Swift / SwiftUI | 5 | 4 | 2 | 5 | 2 | 5 | 3 | 1 | 5 | **70/100** |

## 3.3 Frontend Decision

**Selected Technology: React Native + TypeScript**

React Native achieved the highest weighted score of **93/100**.

It provides the best overall balance of:

- Cross-platform development
- Development speed
- Code reusability
- Ecosystem support
- AI integration
- Real-time integration
- Maintainability
- Development cost

Flutter is a strong alternative, especially for highly shared mobile
and web interfaces. However, React Native provides a better overall
fit for the proposed FitFlow architecture.

---

# 4. Backend Technology Decision Matrix

## 4.1 Criteria and Weights

| Criterion | Weight |
|---|---:|
| Performance | 20% |
| Scalability | 15% |
| Development Speed | 15% |
| Security | 15% |
| AI/ML Integration | 15% |
| Real-Time Support | 10% |
| Maintainability | 10% |
| **Total** | **100%** |

## 4.2 Backend Scores

| Technology | Performance | Scalability | Development Speed | Security | AI/ML | Real-Time | Maintainability | Weighted Total |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Node.js + NestJS** | **4** | **5** | **5** | **4** | **4** | **5** | **5** | **90/100** |
| Python + FastAPI | 4 | 4 | 5 | 4 | 5 | 4 | 4 | **86/100** |
| Go | 5 | 5 | 3 | 5 | 3 | 4 | 4 | **84/100** |

## 4.3 Backend Decision

**Selected Main Backend: Node.js + NestJS**

Node.js with NestJS achieved the highest overall score of **90/100**.

It was selected because it provides:

- High development speed
- Strong scalability
- Excellent real-time support
- Structured modular architecture
- Good maintainability
- TypeScript support
- Easy integration with React Native

### AI Microservice

Although FastAPI was not selected as the main backend, it achieved a
high score because of its excellent AI/ML integration.

Therefore:

**Main Backend:** Node.js + NestJS  
**AI Microservice:** Python + FastAPI

This separates normal application logic from AI-intensive workloads.

---

# 5. Database Technology Decision Matrix

## 5.1 Criteria and Weights

| Criterion | Weight |
|---|---:|
| Security | 20% |
| Scalability | 15% |
| Query Performance | 15% |
| Data Integrity | 15% |
| Real-Time Capability | 15% |
| Cost | 10% |
| Maintainability | 10% |
| **Total** | **100%** |

## 5.2 Database Scores

| Database | Security | Scalability | Query Performance | Data Integrity | Real-Time | Cost | Maintainability | Weighted Total |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **PostgreSQL** | **5** | **4** | **5** | **5** | **3** | **4** | **4** | **87/100** |
| MongoDB | 4 | 5 | 4 | 3 | 3 | 4 | 4 | **77/100** |
| **Cloud Firestore** | **4** | **5** | **4** | **3** | **5** | **4** | **5** | **85/100** |
| DynamoDB | 5 | 5 | 5 | 3 | 4 | 3 | 3 | **83/100** |

## 5.3 Database Decision

### Primary Database: PostgreSQL

PostgreSQL achieved the highest overall score of **87/100**.

It is selected as the primary database because FitFlow contains
structured and highly related information such as:

- User profiles
- Workout plans
- Workout history
- Nutrition records
- Progress records
- Subscription information

PostgreSQL provides strong relational integrity, transaction support,
and complex query capabilities.

### Real-Time Database: Cloud Firestore

Cloud Firestore achieved **85/100** and provides stronger built-in
real-time capabilities than PostgreSQL.

Therefore, a hybrid database architecture is recommended.

**PostgreSQL will store:**

- User profiles
- Workout plans
- Nutrition data
- Progress records
- Subscription data

**Cloud Firestore will store or support:**

- Community posts
- Private fitness circles
- Challenges
- Comments
- Real-time social updates

---

# 6. Authentication Technology Decision Matrix

## 6.1 Criteria and Weights

| Criterion | Weight |
|---|---:|
| Security | 25% |
| Integration | 20% |
| Setup Speed | 15% |
| Scalability | 15% |
| Cost | 10% |
| Maintainability | 15% |
| **Total** | **100%** |

## 6.2 Authentication Scores

| Authentication Solution | Security | Integration | Setup Speed | Scalability | Cost | Maintainability | Weighted Total |
|---|---:|---:|---:|---:|---:|---:|---:|
| **Firebase Authentication** | **4** | **5** | **5** | **5** | **5** | **5** | **95/100** |
| AWS Cognito | 5 | 4 | 3 | 5 | 4 | 3 | **82/100** |
| Auth0 | 5 | 4 | 4 | 5 | 3 | 4 | **86/100** |
| Supabase Auth | 4 | 4 | 5 | 4 | 5 | 4 | **85/100** |

## 6.3 Authentication Decision

**Selected Technology: Firebase Authentication**

Firebase Authentication achieved the highest weighted score of
**95/100**.

It provides:

- Rapid setup
- Mobile SDK support
- Social authentication
- Token-based authentication
- Strong scalability
- Low maintenance requirements
- Easy integration with Firebase services and React Native

Authorization will additionally be enforced by the NestJS backend
using role-based access control and authorization guards.

---

# 7. Final Recommended Technology Stack

Based on the weighted decision matrices, the following technologies
are recommended for the FitFlow redesign.

| System Layer | Selected Technology | Score / Role |
|---|---|---|
| Mobile Frontend | **React Native + TypeScript** | **93/100** |
| Main Backend | **Node.js + NestJS** | **90/100** |
| AI Service | **Python + FastAPI** | Dedicated AI/ML microservice |
| Primary Database | **PostgreSQL** | **87/100** |
| Real-Time Layer | **Cloud Firestore** | **85/100** |
| Authentication | **Firebase Authentication** | **95/100** |
| Caching | **Redis** | Performance optimization |

---

# 8. Final Technology Architecture

The selected FitFlow technology stack is:

```text
React Native + TypeScript
            |
            v
     Firebase Authentication
            |
            v
     Node.js + NestJS
       /     |      \
      /      |       \
     v       v        v
PostgreSQL Firestore FastAPI
                       |
                       v
                    AI / ML

Additional Cache Layer:
Redis