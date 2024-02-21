# Cost Optimization Challenge

### 시나리오
* 현재 온프레미스 데이터센터에서 워크로드를 실행 중입니다.  
* 기존 웹 애플리케이션을 **서울 리젼**의 AWS 환경에서 PoC를 수행할 계획입니다.
* 개발자는 평일 오전 9시부터 오후 6시까지만 필요하므로 개발/테스트 인스턴스를 제외한 모든 가상 머신은 24시간 연중무휴로 실행되어야 합니다.
* 애플리케이션은 매달 1TB의 새로운 데이터를 생성하며 Blob 스토리지에 저장되며 최대 30일 동안 데이터를 보관해야 합니다.
* 모든 데이터는 암호화되어야 합니다.
* 다음은 온프레미스 데이터 센터에 있는 웹 애플리케이션의 인벤토리 목록입니다.

**온프레미스 데이터센터**
| Name  | OS | Application | Disk | On-Prem(vCPU) | On-Prem Memory(GiB) | Avg CPU Utilization(%) | Max CPU Utilization(%)| Avg Mem(GiB) | Max Mem(GiB) | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Application | Linux  | Flask  | 40GB  | 8  | 32  | 50  | 70  | 8  | 24  |
| WebServer01  | Linux | Php & Apache  | 40GB  | 16  | 64  | 10  | 25  | 4  | 20  |
| Redis  | Linux  | Redis v.4 | 40GB  | 4  | 16  | 10  | 20  | 7  | 11  |
| Posgre-Master  | Linux  | PosgreSQL v.13  | 40GB | 4  | 16  | 50  | 70  | 3  | 5  |
| Dev/Test | Linux  | Flask  | 40GB  | 2  | 8  | 40  | 60  | 4  | 6  |
| Blob storage | N/A  | N/A  | 100TB 



**AWS에서의 샘플 아키텍쳐**
![Images/sample-arc.png](/static/costoptimization/getting-started/sample-architecture.png?classes=lab_picture_small)

### Challenge#1

기존 온프레미스 CPU 및 메모리 사양에 따라 Amazon EC2 인스턴스 타입을 선택하고 [AWS Pricing Calculator](https://calculator.aws/#/)를 사용하여 비용을 계산합니다.

**질문: 각 AWS 리소스에 대한 예상 월 비용은 얼마인가요?**


### Challenge#2 

CPU 및 메모리 사용률까지 고려하여 가장 비용 효율적인 Rightsizing을 해보세요. 

**질문: Rightsize된 AWS 리소스에 대한 예상 월별 비용은 얼마인가요?**

* Earning points for challenge#2 vary depending on **Cost Savings opportunity(%)**

> [!IMPORTANT]
> **ℹ️ CPU 사용률이 100%에 도달하지 않아야 합니다.** 


### Challenge#3 

지금까지는 AWS 리소스를 수동으로 권한 크기 조정했습니다. 만약, 인스턴스가 100개가 넘는다면 실제 사용량을 기준으로 어떻게 효율적으로 Rightsizing 해야 할까요? 이러한 경우, 과거 사용률 데이터와 자동화를 통해 비용 절감 기회를 지속적으로 찾아내는 데이터 기반 전략이 필요합니다.

AWS는 아래 그림과 같이 특정 사용 사례에 맞춘 다양한 [AWS 클라우드 재무 관리 서비스](https://aws.amazon.com/aws-cost-management/)를 제공합니다:
![Images/AWSCFMs.png](/static/costoptimization/getting-started/AWSCFMs.png?classes=lab_picture_small)

**질문: 어떤 AWS 클라우드 재무 관리 서비스를 활용하시며, 선택한 이유는 무엇인가요?**

선택한 AWS 클라우드 재무 관리 서비스를 간략하게 설명하고 그 선택의 근거를 설명하는 간단한 프레젠테이션을 작성하세요.

