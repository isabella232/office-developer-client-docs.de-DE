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
ms.openlocfilehash: 1e0c099783b4d44b1aaf746b07c77981c135ca9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19791310"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**Betrifft**: Outlook 
  
Gibt an, ob Microsoft Office Outlook Scannen von Ordnern in einem Speicher und automatisch archiviert werden soll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Eingeblendet auf:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt  <br/> |
|Erstellt:  <br/> |Speicheranbieter  <br/> |
|Durch zugegriffen:  <br/> |Outlook und andere clients  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Zugriffstyp:  <br/> |Nur-Lese- oder Lese-/Schreibzugriff, je nach Speicheranbieter  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren. Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben. [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag. Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PSETID_Common  <br/> |
|UlKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "ArchiveSourceSupportMask"  <br/> |
   
Mit dieser Eigenschaft können Anbieter an, ob Outlook Scannen von Ordnern in einem Speicher und automatisch archiviert werden soll.
  
Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar gemacht bedeutet, dass Outlook-Ordnern auf den Speicher gescannt werden kann. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden die möglichen Werte:
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook kann-Ordnern auf den Speicher gescannt werden.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook sollte-Ordnern auf den Speicher nicht überprüft werden.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- Lassen Sie Clients so ändern Sie diese Eigenschaft im Store nicht zu. Beachten Sie, dass die Konstante **ASM_CLIENT_DO_NOT_CHANGE** für die zukünftige ist und ist derzeit nicht implementiert. Jetzt kann ein Speicher verhindern Clients ändern dieses Flag hartzucodieren der Wert, der der Speicher für diese Eigenschaft zurückgibt. 
    

