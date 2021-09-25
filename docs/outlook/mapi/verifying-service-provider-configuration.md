---
title: Überprüfen der Dienstanbieterkonfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 40da25cd271214c93f894e6540ebb39f362e02b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566213"
---
# <a name="verifying-service-provider-configuration"></a>Überprüfen der Dienstanbieterkonfiguration
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihre Anmeldemethode ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) muss die Konfiguration Ihres Anbieters überprüfen. Dies umfasst die Überprüfung, ob alle für den vollständigen Vorgang erforderlichen Eigenschaften richtig festgelegt sind. Jeder Anbieter erfordert eine andere Anzahl von Eigenschaften. die Konfiguration hängt von Ihrem Anbieter und dem Grad der Benutzerinteraktion ab, die Sie zulassen. Einige Dienstanbieter behalten alle erforderlichen Eigenschaften im Profil. 

Andere Dienstanbieter behalten einen Teilsatz von Eigenschaften im Profil bei und fordern den Benutzer auf, fehlende Werte einzufordern. Andere Anbieter speichern jedoch keine Eigenschaften im Profil und verlassen sich dabei darauf, dass der Benutzer alle für die Konfiguration erforderlichen Informationen zur Verfügung stellt.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>So rufen Sie im Profil gespeicherte Eigenschaften ab
  
1. Rufen Sie [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)auf, und übergeben Sie die [MAPIUID](mapiuid.md) Ihres Anbieters als Eingabeparameter. 
    
2. Rufen Sie die [IMAPIProp::GetProps-](imapiprop-getprops.md) oder [IMAPIPropProp::GetPropList-Methoden](imapiprop-getproplist.md) des Profilabschnitts auf, um einzelne Eigenschaften oder eine Eigenschaftenliste abzurufen. 
    
### <a name="to-set-properties-from-user-information"></a>So legen Sie Eigenschaften aus Benutzerinformationen fest
  
Zeigen Sie ein Eigenschaftenblatt an, wenn die MAPI kein Kennzeichen festgelegt hat, das die Anzeige verbietet. Die folgenden Flags deuten darauf hin, dass eine Benutzeroberfläche nicht angezeigt werden kann.
  
|**Wert**|**Dienstleister**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Adressbuchanbieter  <br/> |
|LOGON_NO_DIALOG  <br/> |Transportanbieter  <br/> |
|MDB_NO_DIALOG  <br/> |Nachrichtenspeicheranbieter  <br/> |
   
Wenn Ihr Anbieter nicht alle Konfigurationseigenschaften im Profil speichert, was eine Benutzerinteraktion erfordert, und MAPI eines der Dialogfeldunterdrückungsflags an Ihre Anmeldemethode übergibt, geben Sie MAPI_E_UNCONFIGURED zurück. Geben Sie diesen Fehler auch zurück, wenn das Dialogfeldunterdrückungs-Flag nicht festgelegt ist, der Benutzer jedoch nicht alle erforderlichen Informationen bereitstellt.
  
Wenn ihr Dienstanbieter seine Anmeldemethode mit MAPI_E_UNCONFIGURED nicht erfolgreich ausführt, ruft MAPI die Einstiegspunktfunktion erneut auf. Wenn die Informationen beim zweiten Aufruf nicht gefunden werden können, wird die Sitzung möglicherweise beendet, je nachdem, wie wichtig Ihr Dienstanbieter ist. 
  
Die folgende Abbildung zeigt die Logik, die für die Konfiguration in der Anmeldemethode des Dienstanbieters erforderlich ist. 
  
**Flussdiagramm für Konfigurationsüberprüfung**
  
![Flussdiagramm für Konfigurationsüberprüfung](media/amapi_62.gif "Flussdiagramm für Konfigurationsüberprüfung")
  
## <a name="see-also"></a>Siehe auch

- [Implementieren der Dienstanbieteranmeldung](implementing-service-provider-logon.md)

