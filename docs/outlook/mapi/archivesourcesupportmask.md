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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281592"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob in Microsoft Office Outlook Ordner in einem Speicher gescannt und automatisch archiviert werden sollen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar unter:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt  <br/> |
|Erstellt von:  <br/> |Speicheranbieter  <br/> |
|Zugriff durch:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschafts:  <br/> |PT_LONG  <br/> |
|Zugriffstyp:  <br/> |Je nach Speicheranbieter schreibgeschützt oder Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMAPIProp: IUnknown](imapipropiunknown.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden. Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben. Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Art. lpwstrName:  <br/> |L "ArchiveSourceSupportMask"  <br/> |
   
Mit dieser Eigenschaft können Speicheranbieter angeben, ob Outlook Ordner in einem Speicher überprüfen und automatisch archivieren soll.
  
Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar, was bedeutet, dass Outlook Ordner im Speicher überprüfen kann. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook kann Ordner im Speicher überprüfen.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook sollte Ordner im Speicher nicht überprüfen.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- Clients dürfen diese Eigenschaft nicht im Speicher ändern. Beachten Sie, dass die Konstante **ASM_CLIENT_DO_NOT_CHANGE** als zukünftige Referenz dient und derzeit nicht implementiert ist. Im Moment kann ein Speicher verhindern, dass Clients dieses Flag ändern, indem der Wert hart codiert wird, den der Store für diese Eigenschaft zurückgibt. 
    

