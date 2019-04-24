---
title: Speichertyp als private Eigenschaft festlegen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298467"
---
# <a name="make-store-type-private-property"></a>Speichertyp als private Eigenschaft festlegen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Behandelt einen sekundären Speicher als privat.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar unter:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt  <br/> |
|Erstellt von:  <br/> |Speicheranbieter  <br/> |
|Zugriff durch:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschafts:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden. Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben. Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Art. lpwstrName:  <br/> |L "urn: Schemas-Microsoft-com: Office: Outlook # storetypeprivate"  <br/> |
   
Ein Informationsspeicher Anbieter kann diese Eigenschaft verwenden, damit Outlook Sie als private behandelt, wenn es sich um einen sekundären Speicher für einen Benutzer handelt. 
  
Standardmäßig behandelt Outlook einen sekundären Speicher auf dieselbe Weise wie ein Stellvertreter Speicher, und Elemente im sekundären Speicher sind nur dann privat, wenn der Benutzer Sie ausdrücklich als privat kennzeichnet. Wenn diese Eigenschaft auf **true**festgelegt ist, werden aus einem sekundären Speicher gelöschte Elemente in den Ordner **Gelöschte Elemente** im primären Speicher verschoben. Als privat gekennzeichnete Elemente werden nicht angezeigt. Entwürfe werden im Ordner "Entwürfe" im primären Speicher gespeichert. 
  
Diese Eigenschaft wird ignoriert, wenn die Version von Outlook älter als Microsoft Office Outlook 2003 Service Pack 1 ist, oder wenn der Wert **false**ist.
  

