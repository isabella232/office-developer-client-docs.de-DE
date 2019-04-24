---
title: Überprüfen der Dienstanbieterkonfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329607"
---
# <a name="verifying-service-provider-configuration"></a>Überprüfen der Dienstanbieterkonfiguration
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihre Anmeldemethode ([IABProvider:: LOGON](iabprovider-logon.md), [IMSProvider:: LOGON](imsprovider-logon.md)oder [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md)) muss die Konfiguration Ihres Anbieters überprüfen. Dabei wird überprüft, ob alle für den vollständigen Vorgang erforderlichen Eigenschaften richtig festgelegt sind. Jeder Anbieter benötigt eine unterschiedliche Anzahl von Eigenschaften; die Konfiguration hängt von Ihrem Anbieter und dem Grad der zulässigen Benutzerinteraktion ab. Einige Dienstanbieter behalten alle erforderlichen Eigenschaften im Profil bei. 

Andere Dienstanbieter behalten eine partielle Gruppe von Eigenschaften im Profil bei und fordern den Benutzer auf, fehlende Werte einzugeben. Dennoch werden von anderen Anbietern keine Eigenschaften im Profil gespeichert, und der Benutzer muss alle für die Konfiguration erforderlichen Informationen bereitstellen.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>So rufen Sie im Profil gespeicherte Eigenschaften ab
  
1. Rufen Sie [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)auf, und übergeben Sie die [MAPIUID](mapiuid.md) Ihres Anbieters als Eingabeparameter. 
    
2. Rufen Sie die Methoden [IMAPIProp::](imapiprop-getprops.md) GetProps oder [IMAPIProp::](imapiprop-getproplist.md) getproplist des profile-Abschnitts auf, um einzelne Eigenschaften oder eine Eigenschaftenliste abzurufen. 
    
### <a name="to-set-properties-from-user-information"></a>So legen Sie Eigenschaften aus Benutzerinformationen fest
  
Zeigt ein Eigenschaftenfenster an, wenn MAPI kein Flag festgelegt hat, das die Anzeige verhindert. Die folgenden Flags zeigen an, dass eine Benutzeroberfläche nicht angezeigt werden kann.
  
|**Wert**|**Dienstanbieter**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Adressbuchanbieter  <br/> |
|LOGON_NO_DIALOG  <br/> |Transport Anbieter  <br/> |
|MDB_NO_DIALOG  <br/> |Nachrichtenspeicher Anbieter  <br/> |
   
Wenn Ihr Anbieter nicht alle Konfigurationseigenschaften im Profil speichert, eine Benutzerinteraktion erfordert und MAPI eines der Dialogfeld Unterdrückungs Kennzeichen an Ihre Anmeldemethode übergibt, geben Sie MAPI_E_UNCONFIGURED zurück. Geben Sie auch diesen Fehler zurück, wenn das Dialogfeld Unterdrückungs Kennzeichen nicht festgelegt ist, aber der Benutzer nicht alle erforderlichen Informationen bereitstellt.
  
Wenn der Dienstanbieter seine Anmeldemethode mit MAPI_E_UNCONFIGURED nicht unterbricht, ruft MAPI ihre Einstiegspunktfunktion erneut auf. Wenn die Informationen beim zweiten Aufruf nicht gefunden werden können, wird die Sitzung möglicherweise beendet, je nachdem, wie wichtig der Dienstanbieter ist. 
  
Die folgende Abbildung zeigt die Logik, die für die Konfiguration in ihrer Dienstanbieter-Anmeldemethode erforderlich ist. 
  
**Flussdiagramm für Konfigurationsüberprüfung**
  
![Flussdiagramm zur Konfigurationsüberprüfung] (media/amapi_62.gif "Flussdiagramm zur Konfigurationsüberprüfung")
  
## <a name="see-also"></a>Siehe auch

- [Implementieren der Dienstanbieter Anmeldung](implementing-service-provider-logon.md)

