---
title: Überprüfen der Konfiguration für Service provider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f6190b2860e227b24b34e31a4ee9741468383460
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589637"
---
# <a name="verifying-service-provider-configuration"></a>Überprüfen der Konfiguration für Service provider
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Logon-Methode ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) muss vom Dienstanbieter Konfiguration überprüfen. Dieser Schritt umfasst, überprüfen, dass alle Eigenschaften für die vollständige Vorgänge benötigt richtig eingestellt sind. Jeder Anbieter erfordert eine unterschiedliche Anzahl von Eigenschaften. Konfiguration abhängig von Ihren Anbieter und den Grad der Benutzerinteraktion, für die Sie zulassen. Einige Dienstanbieter lassen Sie alle erforderlichen Eigenschaften im Benutzerprofil. 

Dienstanbieter lassen Sie eine Teilmenge der Eigenschaften im Benutzerprofil und auffordern, nach fehlenden Werten. Noch speichern andere Anbieter Eigenschaften im Benutzerprofil in allen nicht auf dem Benutzer alle Informationen für die Konfiguration erforderlich ist.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Zum Abrufen von Eigenschaften, die im Profil gespeichert
  
1. Rufen Sie [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), die [MAPIUID](mapiuid.md) Ihres Anbieters als Eingabeparameter übergeben. 
    
2. Rufen Sie Profilabschnitt [IMAPIProp::GetProps](imapiprop-getprops.md) oder [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methoden zum Abrufen von einzelnen Eigenschaften oder eine Eigenschaftenliste auf. 
    
### <a name="to-set-properties-from-user-information"></a>Festlegen von Eigenschaften von Benutzerinformationen
  
Ein Eigenschaftenblatt angezeigt, wenn MAPI ein Flag verbietet die Anzeige nicht festgelegt wurde. Die folgenden Kennzeichen darauf hinzuweisen, dass eine Benutzeroberfläche nicht gestellt werden.
  
|**Wert**|**Dienstanbieter**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |-Adressbuchanbieter  <br/> |
|LOGON_NO_DIALOG  <br/> |Transportdienst  <br/> |
|MDB_NO_DIALOG  <br/> |Nachricht Speicheranbieter  <br/> |
   
Wenn vom Dienstanbieter speichert nicht alle seine Konfigurationseigenschaften in das Profil Benutzereingriff und MAPI zu den Dialogfeld Feld Unterdrückung Flags an Ihre Logon (Methode) übergibt, geben Sie MAPI_E_UNCONFIGURED zurück. Zurückgegeben Sie dieser Fehler wird auch, wenn das Dialogfeld Unterdrückung Flag nicht festgelegt ist, aber der Benutzer nicht alle erforderlichen Informationen bereitstellt.
  
Wenn die Logon-Methode mit MAPI_E_UNCONFIGURED Ihren Dienstanbieter ein Fehler auftritt, ruft MAPI erneut Ihre Entry Point-Funktion. Wenn die Informationen nicht mit dem zweiten Aufruf gefunden werden kann, kann die Sitzung beenden, je nachdem, wie wichtig Ihren Dienstanbieter ist. 
  
Die folgende Abbildung zeigt die Logik für die Konfiguration in Ihrer Service Provider Logon (Methode) erforderlich. 
  
**Flussdiagramm für Konfigurationsüberprüfung**
  
![Flussdiagramm für konfigurationsüberprüfung] (media/amapi_62.gif "Flussdiagramm für konfigurationsüberprüfung")
  
## <a name="see-also"></a>Siehe auch

- [Implementieren einer Dienstanbieteranmeldung](implementing-service-provider-logon.md)

