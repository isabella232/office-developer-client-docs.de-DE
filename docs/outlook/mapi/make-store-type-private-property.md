---
title: Make Store Type Private Property
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428543"
---
# <a name="make-store-type-private-property"></a>Make Store Type Private Property

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Behandelt einen sekundären Speicher als privat.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff durch:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftstyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen. 
  
Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"  <br/> |
   
Ein Speicheranbieter kann diese Eigenschaft verwenden, um Outlook als privat zu behandeln, wenn es sich um einen sekundären Speicher für einen Benutzer handelt. 
  
Standardmäßig behandelt Outlook einen sekundären Speicher auf die gleiche Weise wie ein Stellvertretungsspeicher, und Elemente im sekundären Speicher sind nur dann privat, wenn der Benutzer sie speziell als privat kennzeichnet. Wenn diese Eigenschaft **true ist,** werden elemente, die aus einem sekundären Speicher gelöscht wurden, in den Ordner **Gelöschte** Elemente im primären Speicher verschoben. Als privat markierte Elemente werden nicht angezeigt. Entwürfe werden im Ordner Entwürfe im primären Speicher gespeichert. 
  
Diese Eigenschaft wird ignoriert, wenn die Version von Outlook vor Microsoft Office Outlook 2003 Service Pack 1 liegt oder wenn ihr Wert **false ist.**
  

