---
title: Option-Eigenschaft für Besprechungs Update ausblenden
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299510"
---
# <a name="hide-meeting-update-option-property"></a>Option-Eigenschaft für Besprechungs Update ausblenden

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Blendet die Option zum Senden von Besprechungs Updates an nur hinzugefügte oder gelöschte Teilnehmer aus.
  
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
|Art. lpwstrName:  <br/> |L "urn: Schemas-Microsoft-com: Office: Outlook # allornonemtgupdatedlg"  <br/> |
   
Ein Informationsspeicher Anbieter, der einen Server zum Senden von Besprechungs Updates verwendet, kann das Dialogfeld **Update an Teilnehmer senden** ändern. Diese Funktion ist nützlich, da der Server nicht weiß, welche Teilnehmer seit der anfänglichen Besprechungsanfrage vom Benutzer hinzugefügt oder gelöscht wurden. Wenn diese Eigenschaft auf **true**festgelegt ist, wird die Option **nur Update an hinzugefügte oder gelöschte Teilnehmer senden** nicht im Dialogfeld an **Teilnehmer senden** angezeigt. 
  
Diese Eigenschaft wird ignoriert, wenn die Version von Outlook älter als Microsoft Office Outlook 2003 Service Pack 1 ist, oder wenn der Wert **false**ist.
  

