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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420913"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob in Microsoft Office Outlook Ordner in einem Speicher, einschließlich Kontakte, Kalender und Aufgabenordner, beim Start gescannt werden sollen, um den Navigationsbereich aufzufüllen.
  
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
|Art. lpwstrName:  <br/> |L "CrawlSourceSupportMask"  <br/> |
   
Diese Eigenschaft bietet Speicheranbietern die Möglichkeit, anzugeben, ob Outlook verschiedene Ordner in einem Speicher überprüfen soll. Er wird beim Start verwendet, wenn Outlook vorhandene Ordner in jedem geöffneten Speicher überprüft, um den **Navigations** Bereich zu füllen. Outlook überprüft das vorhanden sein und den Wert dieser Eigenschaft in einem Speicher, bevor die Überprüfung initiiert wird. 
  
Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar, was bedeutet, dass Outlook Ordner im Speicher überprüfen kann. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook kann Ordner im Speicher überprüfen.
    
CSM_DO_NOT_CRAWL
  
- Outlook sollte Ordner im Speicher nicht überprüfen.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Clients dürfen diese Eigenschaft nicht im Speicher ändern. Beachten Sie, dass die Konstante **CSM_CLIENT_DO_NOT_CHANGE** als zukünftige Referenz dient und derzeit nicht implementiert ist. Im Moment kann ein Speicher verhindern, dass Clients dieses Flag ändern, indem der Wert hart codiert wird, den der Store für diese Eigenschaft zurückgibt. 
    

