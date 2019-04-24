---
title: Berechtigungen für MAPI-Objekte und-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4efa9cd1596cffe19a19a62059f81fa553343d77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348594"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Berechtigungen für MAPI-Objekte und-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Zugriffsberechtigung oder der Satz von zulässige-Vorgängen kann ein Merkmal von MAPI-Objekten und von einzelnen Eigenschaften sein, die von diesen Objekten unterstützt werden. Der Objektzugriff wird durch das übergeordnete Objekt des Objekts bestimmt. Für eine Nachricht bestimmt der zugehörige Ordner die Zugriffsberechtigungen. Für einen Messagingbenutzer oder eine Verteilerliste macht der Adressbuchcontainer diese Bestimmung. Wenn sich ein Objekt wie eine Nachricht in zwei Ordnern befindet, können die Berechtigungen für die beiden Kopien des Objekts unterschiedlich sein. 
  
Clients, die diese Objekte verwenden, können die höchste Zugriffsebene anfordern, die für das Objekt zulässig ist, indem Sie das MAPI_BEST_ACCESS-Flag für den [IMAPISession:: OpenEntry](imapisession-openentry.md) -Aufruf festlegen. Je nach dem Dienstanbieter, der das Objekt implementiert, kann dem Client die erforderliche Zugriffsebene gewährt werden. Clients können die Zugriffsebene bestimmen, die Ihnen gewährt wurde, indem Sie die **** Objekt GetProps-Methode zum Abrufen der **PR_ACCESS** ([pidtagaccess (](pidtagaccess-canonical-property.md))-Eigenschaft aufrufen. Da der Dienstanbieter den Wert für diese Eigenschaft jedoch dynamisch generieren muss, wird empfohlen, dass Clients diesen nur bei Bedarf abrufen. 
  
Um zu bestimmen, ob ein Container wie ein Ordner, ein Adressbuchcontainer oder eine Verteilerliste Änderungen zulässt **** , rufen Sie die GetProps-Methode auf, um die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft abzurufen. Der Zugriff auf Container Ebene wirkt sich auf Clients im Hinblick auf die Anzeige Ihrer Benutzeroberflächen aus. Sie wirkt sich auch auf die Implementierung von Objekten innerhalb von Containern im Hinblick auf die Anzeige der Benutzeroberfläche und deren allgemeine Implementierung aus. 
  
Der Zugriff auf eine bestimmte Eigenschaft wird durch das von MAPI für das Objekt, das die Eigenschaft besitzt, festgelegte Eigenschaften Schema bestimmt. Eigenschaftsschemas geben den Satz der erforderlichen und optionalen Eigenschaften für ein Objekt und dessen Zugriffsberechtigungen an. Im Gegensatz zum Objektzugriff, der vom übergeordneten Objekt des Objekts bestimmt wird, ist der Eigenschaftenzugriff Global. Jedes Objekt hat, unabhängig von den Zugriffsanforderungen des übergeordneten Objekts, die gleichen Berechtigungen für die Eigenschaft, die vom Schema bestimmt werden.
  
Wenn eine Eigenschaft schreibgeschützt ist, ist Sie immer mit einem getProps **** -oder **OpenProperty** -Aufruf verfügbar. Je nach der Implementierung des Objekts, das die Eigenschaft unterstützt, gibt es jedoch zwei mögliche Ergebnisse für die **** SetProps-Methode zum Ändern einer Eigenschaft und die **DeleteProps** -Methode zum Entfernen: 
  
- Fail-und Return-MAPI_E_NO_ACCESS
    
- Erfolgreich ohne Aktion
    
Der Zugriff auf Eigenschaften und Objekte kann auch mithilfe der [IPropData](ipropdataimapiprop.md) -Schnittstelle abgerufen oder festgelegt werden, die von der **IMAPIProp** -Schnittstelle erbt. MAPI bietet eine Implementierung von **IPropData** , die auf Daten im Arbeitsspeicher basiert. Dienstanbieter können **IPropData** verwenden, um **IMAPIProp** unter bestimmten Umständen zu implementieren, beispielsweise für Ihr Status-Objekt oder wenn Sie eine Datenbank verwenden, die keine integrierten Transaktionen hat. **IPropData** funktioniert ausschließlich im Arbeitsspeicher, sodass es nicht erforderlich ist, Daten zu sperren und zu entsperren. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

