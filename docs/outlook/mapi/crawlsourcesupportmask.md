---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 550230a104e00123418bfb9b3213c0384e880311
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551807"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob Microsoft Office Outlook ordner in einem Speicher, einschließlich Kontakte, Kalender und Aufgabenordner, beim Start überprüfen soll, um den Navigationsbereich aufzufüllen.
  
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
|Kind.lpwstrName:  <br/> |L"CrawlSourceSupportMask"  <br/> |
   
Diese Eigenschaft bietet Speicheranbietern die Möglichkeit, anzugeben, ob Outlook verschiedene Ordner in einem Speicher überprüfen sollen. Es wird beim Start verwendet, wenn Outlook vorhandene Ordner in jedem geöffneten Speicher überprüft, um den **Navigationsbereich** zu füllen. Outlook überprüft das Vorhandensein und den Wert dieser Eigenschaft in einem Speicher, bevor die Überprüfung initiiert wird. 
  
Standardmäßig wird diese Eigenschaft nicht für einen Speicher verfügbar gemacht, was bedeutet, dass Outlook Ordner im Speicher überprüfen können. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook können Ordner im Speicher überprüfen.
    
CSM_DO_NOT_CRAWL
  
- Outlook sollten keine Ordner im Speicher scannen.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Clients nicht erlauben, diese Eigenschaft im Speicher zu ändern. Beachten Sie, dass die Konstante **CSM_CLIENT_DO_NOT_CHANGE** für zukünftige Verweise vorgesehen ist und derzeit nicht implementiert ist. Derzeit kann ein Speicher verhindern, dass Clients dieses Kennzeichen ändern, indem der Wert, den der Speicher für diese Eigenschaft zurückgibt, hartcodiert wird. 
    

