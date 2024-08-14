# PermitRequestApp

PermitRequestApp, kullanıcıların izin taleplerini yönetmek için geliştirilmiş bir web uygulamasıdır. Bu proje, hem MVC hem de WebAPI mimarilerini içerir ve Clean Architecture prensiplerine göre yapılandırılmıştır.

## Proje Yapısı

### 1. PermitRequestApp.Application
- **Application Katmanı**: Uygulamanın iş mantığını içerir.
  - **Features**: İş kurallarını ve uygulamanın özelliklerini içerir.
  - **Mapping**: Nesne dönüştürme (mapping) işlemleri.
  - **MediatR**: CQRS (Command Query Responsibility Segregation) deseninin uygulanması.
  - **AutoMapper**: Nesneler arasında veri eşleme işlemleri.
  - **Ardalis.Result**: İşlemlerin sonucunu yönetmek ve döndürmek için kullanılır.

### 2. PermitRequestApp.Domain
- **Domain Katmanı**: Uygulamanın çekirdek iş mantığı ve iş kurallarını içerir.
  - **Entities**: Uygulamanın temel veri yapıları ve modelleri.
  - **Abstractions**: Domain arayüzleri.
  - **LeaveRequests, CumulativeLeaveRequests**: İzin talepleri ve toplu izin taleplerini yönetir.
  - **Notifications**: Bildirimler.

### 3. PermitRequestApp.Infrastructure
- **Infrastructure Katmanı**: Uygulamanın altyapı hizmetlerini sağlar.
  - **Repositories**: Veritabanı erişim arayüzlerinin somut implementasyonları.
  - **Migrations**: Veritabanı şema değişikliklerini yönetir.
  - **Entity Framework Core**: Veritabanı işlemleri.

### 4. PermitRequestApp.MVC
- **MVC Katmanı**: Kullanıcı arayüzünü yönetir.
  - **Controllers**: HTTP isteklerini işleyen denetleyiciler.
  - **Views**: Kullanıcıya gösterilen arayüzler.
  - **DTOs**: Veri Transfer Nesneleri.
  - **Models**: Veritabanı modelleri.

### 5. PermitRequestApp.WebAPI
- **WebAPI Katmanı**: Uygulamanın dış dünya ile etkileşime geçtiği katmandır.
  - **Controllers**: API uç noktalarını barındırır.
  - **MediatR**: API'nin iş akışlarını yönetir.
  - **Swashbuckle (Swagger)**: API dokümantasyonu.

## Kullanılan Teknolojiler ve Kütüphaneler
- **ASP.NET Core MVC**
- **Entity Framework Core**
- **AutoMapper**
- **MediatR**
- **Ardalis.Result**
- **Swagger (Swashbuckle)**
