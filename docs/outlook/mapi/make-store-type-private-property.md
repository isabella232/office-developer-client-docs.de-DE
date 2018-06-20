---
title: Stellen Sie Store Typ Private-Eigenschaft
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
ms.openlocfilehash: 7f60d9524af18bb7f2e876386c45b84f207d42bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792937"
---
# <a name="make-store-type-private-property"></a>Stellen Sie Store Typ Private-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Wird einen sekundären Speicher als privat behandelt.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Eingeblendet auf:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt  <br/> |
|Erstellt:  <br/> |Speicheranbieter  <br/> |
|Durch zugegriffen:  <br/> |Outlook und andere clients  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Hinweise

Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren. Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben. [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag. Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|UlKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "Urn: Schemas-Microsoft-Com:office:outlook #storetypeprivate"  <br/> |
   
Ein Anbieter kann diese Eigenschaft verwenden, damit Outlook als privat behandelt, wenn es sich um einen sekundären Speicher für einen Benutzer ist. 
  
In der Standardeinstellung Outlook einen sekundären Speicher behandelt die gleiche Weise wie ein Delegatspeicher und Elemente in den sekundären Speicher private nur, wenn der Benutzer diese speziell als privat markiert sind. Wenn diese Eigenschaft auf **true**festgelegt ist, werden in den Ordner **Gelöschte Objekte** in den primären Speicher in einem sekundären Speicher gelöschte Elemente verschoben. Als privat gekennzeichnete Elemente werden nicht angezeigt. Entwürfe werden im Ordner "Entwürfe" in den primären Speicher gespeichert. 
  
Diese Eigenschaft wird ignoriert, wenn die Version von Outlook einer älteren Version als Microsoft Office Outlook 2003 Service Pack 1 ist oder wenn der Wert **false**lautet.
  

