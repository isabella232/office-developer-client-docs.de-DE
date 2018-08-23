---
title: Berechtigungen für die MAPI-Objekten und Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 11c8a58e6cfe0719e8683c4e7a0fd966972117c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569379"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Berechtigungen für die MAPI-Objekten und Eigenschaften

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zugriffsberechtigung oder eine Reihe von Operationen zulässig sind, kann ein Merkmal des MAPI-Objekten und einzelner Eigenschaften von diesen Objekten unterstützt. Objektzugriff wird vom übergeordneten Objekts bestimmt. Für eine Nachricht bestimmt der Ordner Zugriffsberechtigungen. Ein messaging-Benutzer oder eine Verteilerliste wird seine Adressbuchcontainer hierbei. Wenn ein Objekt wie eine Nachricht in zwei Ordner befindet, können die Berechtigungen für die zwei Kopien des Objekts abweichen. 
  
Clients, die diese Objekte verwenden, können die höchste Zugriffsebene für das Objekt durch das MAPI_BEST_ACCESS-Flag für den Anruf [IMAPISession::OpenEntry](imapisession-openentry.md) festlegen zugelassen anfordern. Je nach den Dienstanbieter, die das Objekt implementieren wird der Client kann oder kann nicht die Zugriffsebene erforderlichen erteilt werden. Clients können die Zugriffsebene bestimmen, dass sie erteilt wurden durch Aufrufen des Objekts **GetProps** -Methode, um die Eigenschaft **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) abzurufen. Allerdings, da der Dienstanbieter dynamisch generieren des Werts für diese Eigenschaft muss, wird empfohlen, dass Clients diese nur bei Bedarf abgerufen werden. 
  
Um festzustellen, ob ein Container wie ein Ordner, Adressbuchcontainer oder Verteilerliste können Sie ändern, rufen Sie seine **GetProps** -Methode zum Abrufen der Eigenschaft **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). Die Zugriffsebene Container wirkt sich auf Clients im Hinblick auf die Art der Anzeige ihrer von Benutzeroberflächen. Sie beeinflusst auch die Implementierung von in Containern im Hinblick auf die Anzeige ihrer Benutzer-Schnittstelle und deren allgemeine Implementierung-Objekten. 
  
Zugriff auf eine bestimmte Eigenschaft wird durch das Einrichten von MAPI für das Objekt, das die Eigenschaft besitzt Eigenschaftsschema bestimmt. Eigenschaftenschemas angeben die erforderlichen und optionalen Eigenschaften für ein Objekt und deren Berechtigungen. Im Gegensatz zum Zugriff auf Objekte, die durch das übergeordnete Objekt bestimmt wird, ist der Zugriff auf Eigenschaften global. Jedes Objekt, unabhängig von der Access-Anforderungen, der das übergeordnete Objekt, hat die gleichen Berechtigungen für die Eigenschaft, wie durch das Schema bestimmt.
  
Wenn eine Eigenschaft schreibgeschützt ist, wird es immer mit einem Aufruf **GetProps** oder **OpenProperty** verfügbar sein. Je nach der Implementierung des Objekts die Eigenschaft unterstützt, sind jedoch für die **SetProps** -Methode zum Ändern einer Eigenschaft und die **"DeleteProps"** -Methode zum Entfernen von es zwei mögliche Ergebnisse: 
  
- Fehler und return MAPI_E_NO_ACCESS
    
- Keine Aktion ausgeführt erfolgreich
    
Access-Eigenschaft und -Objekt kann auch abgerufen oder mithilfe der [IPropData](ipropdataimapiprop.md) -Schnittstelle, die von der **IMAPIProp** -Schnittstelle erbt festgelegt werden. MAPI bietet eine Implementierung der **IPropData** , die auf Daten im Arbeitsspeicher basiert. Dienstanbieter können **IPropData** **IMAPIProp** unter bestimmten Umständen wie für ihren Statusobjekt implementieren, oder wenn sie eine Datenbank verwenden, die keine integrierter Transaktionen. **IPropData** funktioniert ausschließlich im Speicher, wodurch es nicht erforderlich, Sperren und Entsperren von Daten. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

