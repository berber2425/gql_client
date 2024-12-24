# Berber GraphQL Client

Berber platformunun GraphQL client kütüphanesi. Bu kütüphane, backend servisleriyle iletişim için gerekli query ve mutation'ları içerir.

## Özellikler

- GraphQL query'leri
- GraphQL mutation'ları
- TypeScript/JavaScript tipler
- Dart tipler (Flutter uygulamaları için)
- GraphQL Code Generator entegrasyonu

## Teknik Detaylar

### Kullanılan Teknolojiler

- GraphQL
- TypeScript
- GraphQL Code Generator
- Node.js

### Geliştirme Ortamı Gereksinimleri

- Node.js
- VS Code veya WebStorm
- Git

### Kurulum

1. Repository'yi klonlayın

```bash
git clone https://github.com/berber2425/gql_client.git
```

2. Bağımlılıkları yükleyin

```bash
npm install
```

3. Tipleri oluşturun

```bash
npm run codegen
```

## Proje Yapısı

```
src/
  ├── queries/        # GraphQL query'leri
  │   ├── auth/       # Kimlik doğrulama
  │   ├── user/       # Kullanıcı işlemleri
  │   ├── org/        # Organizasyon işlemleri
  │   └── admin/      # Admin işlemleri
  ├── mutations/      # GraphQL mutation'ları
  │   ├── auth/       # Kimlik doğrulama
  │   ├── user/       # Kullanıcı işlemleri
  │   ├── org/        # Organizasyon işlemleri
  │   └── admin/      # Admin işlemleri
  ├── fragments/      # Paylaşılan GraphQL parçaları
  └── types/          # Üretilen tipler
```

## Kullanım

### TypeScript/JavaScript

```typescript
import { UserQueries, UserMutations } from "@berber/gql-client";

// Query örneği
const user = await UserQueries.getUser({ id: "user-id" });

// Mutation örneği
const updatedUser = await UserMutations.updateUser({
  id: "user-id",
  data: { name: "Yeni İsim" },
});
```

### Dart/Flutter

```dart
import 'package:berber_gql_client/berber_gql_client.dart';

// Query örneği
final user = await UserQueries.getUser(GetUserArgs(id: 'user-id'));

// Mutation örneği
final updatedUser = await UserMutations.updateUser(
  UpdateUserArgs(
    id: 'user-id',
    data: UpdateUserData(name: 'Yeni İsim'),
  ),
);
```

## Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'feat: add amazing feature'`)
4. Branch'inizi push edin (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun
