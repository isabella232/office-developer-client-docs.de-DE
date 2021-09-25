---
title: Bewährte Methoden für schnelles Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 778bd83e1b75ffdf494bc56cf79a5393e0c975ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572095"
---
# <a name="best-practices-for-fast-shutdown"></a>Bewährte Methoden für schnelles Herunterfahren

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden bewährte Methoden für Administratoren, MAPI-Clients und MAPI-Anbieter empfohlen, um Windows Registrierungseinstellungen und die Schnittstellen für schnelles Herunterfahren zu verwenden, um Datenverluste beim Herunterfahren des Clients zu minimieren.
  
- Damit ein MAPI-Client schnelles Herunterfahren erfolgreich ausführt, damit bei Anbieterprozessen kein Datenverlust auftritt, sollte der MAPI-Client zuerst die [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) aufrufen. Der Client sollte dann mit den Methoden [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) fortfahren, die auf der Unterstützung des MAPI-Subsystems für schnelles Herunterfahren basieren, wie durch den Rückgabewert von **IMAPIClientShutdown::QueryFastShutdown** angegeben. Als MAPI-Client ruft Microsoft Outlook **IMAPIClientShutdown::NotifyProcessShutdown** oder **IMAPIClientShutdown::D oFastShutdown** nicht auf, wenn **IMAPIClientShutdown::QueryFastShutdown** einen Fehler zurückgibt. Wenn der Administrator das schnelle Herunterfahren in der Windows Registrierung deaktiviert hat, würde das MAPI-Subsystem MAPI_E_NO_SUPPORT an **IMAPIClientShutdown::QueryFastShutdown** zurückgeben. In diesem Fall informiert das MAPI-Subsystem MAPI-Anbieter nicht über das sofortige Beenden des Clientprozesses. Wenn ein MAPI-Client diesen Fehlerrückgabecode ignoriert, das schnelle Herunterfahren fortschreitet und alle externen Verweise trennt, gehen bei allen geladenen MAPI-Anbietern Daten verloren. 
    
- MAPI-Anbieter sollten die [IMAPIProviderShutdown : IUnknown-Schnittstelle](imapiprovidershutdowniunknown.md) implementieren, um rechtzeitige und erforderliche Schritte auszuführen, um Datenverluste zu vermeiden, da der Client externe Verweise trennt, bevor der Client beendet wird. Ein Anbieter sollte alle anderen Elemente verschieben, die nicht zum Speichern von Daten in seinem primären Datenspeicher erforderlich sind. Beispielsweise sollte ein Transportanbieter unnötige Hintergrundvorgänge verschieben, die nach neuen E-Mails suchen. Ein Adressbuchanbieter sollte das Herunterladen der letzten Änderungen vom Server verschieben, und ein Speicheranbieter sollte Wartungsaufgaben wie komprimieren oder indizieren verschieben. 
    
- Benutzer, die MAPI-Clients beenden möchten, sobald sie sie schließen, sollten die Standardregistrierungseinstellung verwenden, die ein schnelles Herunterfahren ermöglicht, es sei denn, ein Anbieter opts out.
    
- Sobald ein MAPI-Client **IMAPIClientShutdown::D oFastShutdown** aufruft, sollte er keine weiteren Aufrufe an die MAPI vornehmen, einschließlich der [MAPIUninitialize-Funktion.](mapiuninitialize.md) Der Client sollte die MAPI für den Rest der Lebensdauer des Clientprozesses nicht verwenden. 
    
- Ein MAPI-Client sollte niemals direkt die **IMAPIProviderShutdown-Schnittstelle** eines Anbieters aufrufen. MAPI-Clients sollten immer die [IMAPIClientShutdown : IUnknown-Schnittstelle](imapiclientshutdowniunknown.md) verwenden. 
    
- Wenn ein MAPI-Anbieter sicherstellen muss, dass das schnelle Herunterfahren während des Ladens nicht verwendet wird, sollte er die **IMAPIProviderShutdown-Schnittstelle** implementieren und MAPI_E_NO_SUPPORT für die **IMAPIProviderShutdown::QueryFastShutdown-Methode** zurückgeben. Für MAPI-Clients wie Outlook führt dies jedoch dazu, dass der Client das schnelle Herunterfahren aufgibt und länger dauert, bis er heruntergefahren wird. 
    
## <a name="see-also"></a>Siehe auch



[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
  
[Übersicht über das schnelle Herunterfahren](fast-shutdown-overview.md)
  
[Benutzeroptionen für schnelles Herunterfahren](fast-shutdown-user-options.md)

