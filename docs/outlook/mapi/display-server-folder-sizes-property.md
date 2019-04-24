---
title: Display Server Folder sizes-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337079"
---
# <a name="display-server-folder-sizes-property"></a>Display Server Folder sizes-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt die Größe der angegebenen Ordner auf dem Server im Dialogfeld Outlook- **Ordnergröße** an. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar unter:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt  <br/> |
|Erstellt von:  <br/> |Speicheranbieter  <br/> |
|Zugriff durch:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschafts:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMAPIProp: IUnknown](imapipropiunknown.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden. Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben. Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Art. lpwstrName:  <br/> |L "urn: Schemas-Microsoft-com: Office: Outlook # serverfoldersizes"  <br/> |
   
Diese Eigenschaft wird in Microsoft Outlook 2003 Service Pack (SP) 1 unterstützt. Wenn die Version von Outlook älter als Outlook 2003 SP 1 ist oder wenn der Wert **false**ist, zeigt Outlook nur die Größe der Ordner im lokalen Speicher an. Wenn diese Eigenschaft in einem Speicher festgelegt ist, der Outlook 2003 SP 1 verwendet, fragt Outlook die Größe jedes angegebenen Ordners auf dem Server und dem lokalen Laufwerk ab. 
  
Um die Ordnergröße auf dem Server abzufragen, öffnet Outlook einen Ordner im Store mit [IMsgStore:: OpenEntry](imsgstore-openentry.md), übergibt das Flag **MAPI_NO_CACHE**und fragt dann nach **PR_MESSAGE_SIZE_EXTENDED**. Der Informationsspeicher Anbieter sollte dann die Größe des Ordners auf dem Server zurückgeben.
  
Wenn Sie die Größe eines Ordners auf dem lokalen Laufwerk Abfragen möchten, wird der Ordner ohne das **MAPI_NO_CACHE** -Flag geöffnet. Dann fragt Sie nach **PR_MESSAGE_SIZE_EXTENDED**; der Informationsspeicher Anbieter sollte die Größe des angegebenen Ordners auf dem lokalen Laufwerk zurückgeben.
  
Mit dieser Eigenschaft können Speicheranbieter, die Speicherinhalte mit einem Server synchronisieren, Daten auf dem Server im Dialogfeld Outlook- **Ordner** Größe anzeigen. Benutzer können dann Ihre aktuelle Server Speicherauslastung mit Server Kontingenten vergleichen. 
  

