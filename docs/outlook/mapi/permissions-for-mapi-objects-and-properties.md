---
title: Berechtigungen für MAPI-Objekte und -Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: adc960182a7d6a8eeacfcd5ee644c0e2fde9d3d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591976"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Berechtigungen für MAPI-Objekte und -Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zugriffsberechtigungen oder der Satz zulässiger Vorgänge können ein Merkmal von MAPI-Objekten und von einzelnen Eigenschaften sein, die von diesen Objekten unterstützt werden. Der Objektzugriff wird durch das übergeordnete Objekt eines Objekts bestimmt. Für eine Nachricht bestimmt der Ordner Zugriffsberechtigungen. Für einen Messagingbenutzer oder eine Verteilerliste wird dies vom Adressbuchcontainer festgelegt. Wenn sich ein Objekt wie eine Nachricht in zwei Ordnern befindet, können die Berechtigungen für die beiden Kopien des Objekts unterschiedlich sein. 
  
Clients, die diese Objekte verwenden, können die höchste Zugriffsebene anfordern, die für das Objekt zulässig ist, indem sie das MAPI_BEST_ACCESS Flag für den [IMAPISession::OpenEntry-Aufruf](imapisession-openentry.md) festlegen. Abhängig vom Dienstanbieter, der das Objekt implementiert, kann dem Client die erforderliche Zugriffsebene gewährt werden. Clients können die Zugriffsebene bestimmen, die ihnen gewährt wurde, indem sie die **GetProps-Methode** des Objekts aufrufen, um die **eigenschaft PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) abzurufen. Da der Dienstanbieter den Wert für diese Eigenschaft jedoch dynamisch generieren muss, wird empfohlen, dass Clients ihn nur bei Bedarf abrufen. 
  
Rufen Sie die **GetProps-Methode** auf, um zu bestimmen, ob ein Container wie ein Ordner, ein Adressbuchcontainer oder eine Verteilerliste änderungen erlaubt, um die **eigenschaft PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) abzurufen. Der Zugriff auf Containerebene wirkt sich hinsichtlich der Anzeige der Benutzeroberflächen auf Clients aus. Es wirkt sich auch auf die Implementierer von Objekten innerhalb von Containern hinsichtlich der Anzeige der Benutzeroberfläche und ihrer allgemeinen Implementierung aus. 
  
Der Zugriff auf eine bestimmte Eigenschaft wird durch das von mapi für das Objekt eingerichtete Eigenschaftenschema bestimmt, das die Eigenschaft besitzt. Eigenschaftenschemas geben den Satz der erforderlichen und optionalen Eigenschaften für ein Objekt und deren Zugriffsberechtigung an. Im Gegensatz zum Objektzugriff, der vom übergeordneten Objekt bestimmt wird, ist der Eigenschaftszugriff global. Jedes Objekt verfügt unabhängig von den Zugriffsanforderungen des übergeordneten Objekts über die gleichen Berechtigungen für die Eigenschaft, wie durch das Schema bestimmt.
  
Wenn eine Eigenschaft schreibgeschützt ist, ist sie immer mit einem **GetProps-** oder **OpenProperty-Aufruf** verfügbar. Abhängig von der Implementierung des Objekts, das die Eigenschaft unterstützt, gibt es jedoch zwei mögliche Ergebnisse für die **SetProps-Methode** zum Ändern einer Eigenschaft und die **DeleteProps-Methode** zum Entfernen der Eigenschaft: 
  
- Fail and return MAPI_E_NO_ACCESS
    
- Erfolgreich, ohne dass eine Aktion ausgeführt wurde
    
Der Zugriff auf Eigenschaften und Objekte kann auch mithilfe der [IPropData-Schnittstelle](ipropdataimapiprop.md) abgerufen oder festgelegt werden, die von der **IMAPIProp-Schnittstelle** erbt. MAPI stellt eine Implementierung von **IPropData** bereit, die auf Daten im Arbeitsspeicher basiert. Dienstanbieter können **IPropData** verwenden, um **IMAPIProp** unter bestimmten Umständen zu implementieren, z. B. für ihr Statusobjekt oder wenn sie eine Datenbank ohne integrierte Transaktionen verwenden. **IPropData** arbeitet ausschließlich im Arbeitsspeicher, sodass es nicht erforderlich ist, Daten zu sperren und zu entsperren. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

