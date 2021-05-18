---
title: Option "Besprechungsupdate ausblenden"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412100"
---
# <a name="hide-meeting-update-option-property"></a>Option "Besprechungsupdate ausblenden"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Blendet die Option zum Senden von Besprechungsupdates nur an hinzugefügte oder gelöschte Teilnehmer aus.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff durch:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftstyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen. 
  
Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"  <br/> |
   
Ein Speicheranbieter, der einen Server zum Senden von Besprechungsupdates verwendet, kann das Dialogfeld **Update an Teilnehmer** senden ändern. Diese Funktionalität ist nützlich, da der Server beim Senden eines Besprechungsupdates nicht weiß, welche Teilnehmer seit der ersten Besprechungsanfrage vom Benutzer hinzugefügt oder gelöscht wurden. Wenn diese Eigenschaft **true** ist, wird die Option Update nur für hinzugefügte oder gelöschte Teilnehmer senden nicht im Dialogfeld Update an **Teilnehmer** senden angezeigt.  
  
Diese Eigenschaft wird ignoriert, wenn die Version von Outlook vor Microsoft Office Outlook 2003 Service Pack 1 liegt oder wenn ihr Wert **false ist.**
  

