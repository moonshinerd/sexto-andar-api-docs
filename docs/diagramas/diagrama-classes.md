# Diagrama de Classes

## Diagrama

<iframe frameborder="0" style="width:100%;height:606px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=000000&edit=_blank&layers=1&nav=1&title=sextoAndar.drawio&dark=auto#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1czhcvyhd-4xzXKPgRcarmGn223SelN_o%26export%3Ddownload"></iframe>

## Classes Principais

### Account (Classe Abstrata)
- `id: UUID`
- `username: String`
- `fullName: String`
- `phoneNumber: String`
- `email: EmailType`
- `password: String`

### User
Herda de Account

### PropertyOwner
Herda de Account

### Property
- `id: UUID`
- `idPropertyOwner: UUID`
- `propertySize: Numeric(10,10)`
- `description: String`
- `propertyValue: Numeric(10,2)`
- `publishDate: DateTime`
- `condominiumFee: Numeric(10,2)`
- `commonArea: Boolean`
- `floor: Integer`
- `isPetAllowed: Boolean`

### Proposal
- `id: UUID`
- `idProperty: UUID`
- `idUser: UUID`
- `proposalDate: DateTime`
- `proposalValue: Numeric(10,2)`

### Visit
- `id: UUID`
- `idProperty: UUID`
- `idUser: UUID`
- `visitDate: DateTime`
- `isVisitCompleted: Boolean`

### Address
- `id: UUID`
- `street: String`
- `number: String`
- `city: String`
- `postal_code: String`
- `country: String`

## Enumerações

### SalesType
- Rent (Aluguel)
- Sale (Venda)

### PropertyType
- Apartment (Apartamento)
- House (Casa)

## Relacionamentos

1. Account → User, PropertyOwner (Herança)
2. PropertyOwner 1 → 0..* Property
3. Property 1 ←→ 1 Address
4. Property 1 → 0..* Visit
5. Property 1 → 0..* Proposal
6. User 1 → 0..* Visit
7. User 1 → 0..* Proposal
