---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2afdfffe3af123fd9ab3a2c7b06f386bd253bdae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567851"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob Microsoft Office Outlook Ordner in einem Speicher überprüfen und automatisch archivieren sollen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff von:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Zugriffstyp:  <br/> |Schreibgeschützt oder Lese-/Schreibzugriff je nach Store-Anbieter  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftentag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store Anbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter  _"lppPropNames"_ zeigt:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"ArchiveSourceSupportMask"  <br/> |
   
Mit dieser Eigenschaft können Speicheranbieter angeben, ob Outlook Ordner in einem Speicher überprüfen und automatisch archivieren sollen.
  
Standardmäßig wird diese Eigenschaft nicht für einen Speicher verfügbar gemacht, was bedeutet, dass Outlook Ordner im Speicher überprüfen können. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook können Ordner im Speicher überprüfen.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook sollten keine Ordner im Speicher scannen.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- Clients nicht erlauben, diese Eigenschaft im Speicher zu ändern. Beachten Sie, dass die Konstante **ASM_CLIENT_DO_NOT_CHANGE** für zukünftige Verweise vorgesehen ist und derzeit nicht implementiert ist. Derzeit kann ein Speicher verhindern, dass Clients dieses Kennzeichen ändern, indem der Wert, den der Speicher für diese Eigenschaft zurückgibt, hartcodiert wird. 
    

