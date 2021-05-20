---
title: Berechtigungen für MAPI-Objekte und -Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4efa9cd1596cffe19a19a62059f81fa553343d77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436174"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Berechtigungen für MAPI-Objekte und -Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Zugriffsberechtigung oder der Satz zulässiger Vorgänge kann ein Merkmal von MAPI-Objekten und einzelnen Eigenschaften sein, die von diesen Objekten unterstützt werden. Der Objektzugriff wird durch das übergeordnete Objekt eines Objekts bestimmt. Für eine Nachricht bestimmt der Ordner zugriffsberechtigungen. Für einen Messagingbenutzer oder eine Verteilerliste wird diese Bestimmung im Adressbuchcontainer bestimmt. Wenn sich ein Objekt wie eine Nachricht in zwei Ordnern befindet, können die Berechtigungen für die beiden Kopien des Objekts unterschiedlich sein. 
  
Clients, die diese Objekte verwenden, können die höchste Zugriffsebene anfordern, die für das Objekt zulässig ist, indem sie das MAPI_BEST_ACCESS für den [IMAPISession::OpenEntry-Aufruf](imapisession-openentry.md) festlegen. Abhängig vom Dienstanbieter, der das Objekt implementieren, kann dem Client möglicherweise die erforderliche Zugriffsebene gewährt werden. Clients können die Zugriffsebene bestimmen, die ihnen gewährt wurde, indem sie die **GetProps-Objektmethode** aufrufen, um die **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) -Eigenschaft abzurufen. Da der Dienstanbieter den Wert für diese Eigenschaft jedoch dynamisch generieren muss, wird empfohlen, dass Clients ihn nur bei Bedarf abrufen. 
  
Um zu bestimmen, ob ein Container wie z. B. ein Ordner, ein Adressbuchcontainer oder eine Verteilerliste Änderungen zulässt, rufen Sie die **GetProps-Methode** auf, um die **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) -Eigenschaft abzurufen. Der Zugriff auf Containerebene wirkt sich auf Clients im Hinblick auf die Anzeige ihrer Benutzeroberflächen aus. Es wirkt sich auch auf die Implementierer von Objekten in Containern in Bezug auf die Anzeige der Benutzeroberfläche und deren allgemeine Implementierung aus. 
  
Der Zugriff auf eine bestimmte Eigenschaft wird durch das von MAPI für das Objekt, das die Eigenschaft besitzt, eingerichteten Eigenschaftsschema bestimmt. Eigenschaftsschemas geben den Satz der erforderlichen und optionalen Eigenschaften für ein Objekt und deren Zugriffsberechtigung an. Im Gegensatz zum Objektzugriff, der vom übergeordneten Objekt bestimmt wird, ist der Eigenschaftszugriff global. Jedes Objekt verfügt unabhängig von den Zugriffsanforderungen des übergeordneten Objekts über die gleichen Berechtigungen für die Eigenschaft wie durch das Schema bestimmt.
  
Wenn eine Eigenschaft schreibgeschützt ist, ist sie immer mit einem **GetProps-** oder **OpenProperty-Aufruf** verfügbar. Je nach Implementierung des Objekts, das die Eigenschaft unterstützt, gibt es jedoch zwei mögliche Ergebnisse für die **SetProps-Methode** zum Ändern einer Eigenschaft und die **DeleteProps-Methode** zum Entfernen: 
  
- Fehler und Rückgabe MAPI_E_NO_ACCESS
    
- Erfolg ohne Ergriffene Aktion
    
Der Eigenschaften- und Objektzugriff kann auch mithilfe der [IPropData-Schnittstelle](ipropdataimapiprop.md) abgerufen oder festgelegt werden, die von der **IMAPIProp-Schnittstelle erbt.** MAPI bietet eine Implementierung von **IPropData,** die auf Daten im Arbeitsspeicher basiert. Dienstanbieter können **IPropData** verwenden, um **IMAPIProp** unter bestimmten Umständen zu implementieren, z. B. für ihr Statusobjekt oder wenn sie eine Datenbank verwenden, die keine integrierten Transaktionen enthält. **IPropData** funktioniert ausschließlich im Arbeitsspeicher, was das Sperren und Entsperren von Daten unnötig macht. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

