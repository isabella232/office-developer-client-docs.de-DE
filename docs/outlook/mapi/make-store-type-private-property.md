---
title: Make Store Type Private-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8282b5613571a230ba286e0369d6508f6f9d1aec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610363"
---
# <a name="make-store-type-private-property"></a>Make Store Type Private-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Behandelt einen sekundären Speicher als privat.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff von:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftentag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store Anbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter  _"lppPropNames"_ zeigt:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"  <br/> |
   
Ein Speicheranbieter kann diese Eigenschaft verwenden, um Outlook sie als privat zu behandeln, wenn es sich um einen sekundären Speicher für einen Benutzer handelt. 
  
Standardmäßig behandelt Outlook einen sekundären Speicher genauso wie ein Delegatspeicher, und Elemente im sekundären Speicher sind nur privat, wenn der Benutzer sie explizit als privat markiert. Wenn diese Eigenschaft **"true"** ist, werden aus einem sekundären Speicher gelöschte Elemente in den Ordner **"Gelöschte Elemente"** im primären Speicher verschoben. Elemente, die als privat markiert sind, werden nicht angezeigt. Entwürfe werden im Ordner "Entwürfe" im primären Speicher gespeichert. 
  
Diese Eigenschaft wird ignoriert, wenn die Version von Outlook älter als Microsoft Office Outlook 2003 Service Pack 1 ist oder wenn der Wert **"false"** lautet.
  

