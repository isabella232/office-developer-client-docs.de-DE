---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1754a7c82d7164617c97df97b762efb1555ccda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791473"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Betrifft**: Outlook 
  
Gibt an, ob Microsoft Office Outlook-Ordner in einem Speicher, einschließlich Kontakte, Kalender und Aufgaben Ordner, auf Start, um das Füllen Sie im Navigationsbereich gescannt werden sollen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Eingeblendet auf:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt  <br/> |
|Erstellt:  <br/> |Speicheranbieter  <br/> |
|Durch zugegriffen:  <br/> |Outlook und andere clients  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Zugriffstyp:  <br/> |Nur-Lese- oder Lese-/Schreibzugriff, je nach Speicheranbieter  <br/> |
   
## <a name="remarks"></a>Hinweise

Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren. Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben. [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag. Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PSETID_Common  <br/> |
|UlKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "CrawlSourceSupportMask"  <br/> |
   
Diese Eigenschaft bietet eine Möglichkeit für den Anbieter an, ob Outlook verschiedenen Ordnern in einem Speicher gescannt werden sollen. Beim Starten wird verwendet, wenn Outlook führt eine Überprüfung auf vorhandene Ordner für jede geöffnete Speicher zum Auffüllen im **Navigationsbereich** ; Outlook überprüft das Vorhandensein und der Wert dieser Eigenschaft in einem Speicher, bevor die Überprüfung initiieren. 
  
Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar gemacht bedeutet, dass Outlook-Ordnern auf den Speicher gescannt werden kann. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden die möglichen Werte:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook kann-Ordnern auf den Speicher gescannt werden.
    
CSM_DO_NOT_CRAWL
  
- Outlook sollte-Ordnern auf den Speicher nicht überprüft werden.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Lassen Sie Clients so ändern Sie diese Eigenschaft im Store nicht zu. Beachten Sie, dass die Konstante **CSM_CLIENT_DO_NOT_CHANGE** für die zukünftige ist und ist derzeit nicht implementiert. Jetzt kann ein Speicher verhindern Clients ändern dieses Flag hartzucodieren der Wert, der der Speicher für diese Eigenschaft zurückgibt. 
    

