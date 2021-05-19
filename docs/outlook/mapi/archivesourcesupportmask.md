---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418092"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, Microsoft Office Outlook Ordner in einem Speicher überprüfen und automatisch archivieren soll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff durch:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftstyp:  <br/> |PT_LONG  <br/> |
|Zugriffstyp:  <br/> |Schreibgeschützt oder Lese-/Schreibzugriff je nach Speicheranbieter  <br/> |
   
## <a name="remarks"></a>Hinweise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen. 
  
Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"ArchiveSourceSupportMask"  <br/> |
   
Mit dieser Eigenschaft können Speicheranbieter angeben, Outlook Ordner in einem Speicher überprüfen und automatisch archivieren sollen.
  
Diese Eigenschaft wird standardmäßig nicht in einem Speicher verfügbar gemacht, was bedeutet, Outlook Ordner im Speicher überprüfen können. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:
  
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
  
- Outlook sollten keine Ordner im Speicher überprüfen.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- Lassen Sie nicht zu, dass Clients diese Eigenschaft im Store ändern. Beachten Sie, dass die **konstante ASM_CLIENT_DO_NOT_CHANGE** zur zukünftigen Referenz verwendet wird und derzeit nicht implementiert ist. Derzeit kann ein Speicher verhindern, dass Clients dieses Kennzeichen ändern, indem der Wert hartcodiert wird, den der Speicher für diese Eigenschaft zurückgibt. 
    

