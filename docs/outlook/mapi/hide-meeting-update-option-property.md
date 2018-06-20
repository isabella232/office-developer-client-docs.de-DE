---
title: Ausblenden der Besprechung Update Option-Eigenschaft
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
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791830"
---
# <a name="hide-meeting-update-option-property"></a>Ausblenden der Besprechung Update Option-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Blendet die Option zum besprechungsaktualisierungen auf nur hinzugefügte oder gelöschte Teilnehmer senden.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Eingeblendet auf:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt  <br/> |
|Erstellt:  <br/> |Speicheranbieter  <br/> |
|Durch zugegriffen:  <br/> |Outlook und andere clients  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Hinweise

Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren. Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben. [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag. Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|UlKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "Urn: Schemas-Microsoft-Com:office:outlook #allornonemtgupdatedlg"  <br/> |
   
Ein Anbieter anmelden, der einen Server verwendet, um die Besprechung aktualisiert senden kann das Dialogfeld **Aktualisierung an Teilnehmer senden** ändern. Diese Funktion ist hilfreich, da bei der Server eine besprechungsaktualisierung sendet, der Server nicht bekannt ist, welche Teilnehmer hinzugefügt oder vom Benutzer gegenüber der ursprünglichen Besprechungsanfrage gelöscht wurden. Wenn diese Eigenschaft auf **true**festgelegt ist, wird die Option **Update nur für hinzugefügten oder gelöschten Teilnehmer senden** nicht im Dialogfeld **Aktualisierung an Teilnehmer senden** angezeigt. 
  
Diese Eigenschaft wird ignoriert, wenn die Version von Outlook einer älteren Version als Microsoft Office Outlook 2003 Service Pack 1 ist oder wenn der Wert **false**lautet.
  

