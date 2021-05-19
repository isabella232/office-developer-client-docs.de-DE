---
title: Überprüfen der Dienstanbieterkonfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418848"
---
# <a name="verifying-service-provider-configuration"></a>Überprüfen der Dienstanbieterkonfiguration
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihre Anmeldemethode ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) muss die Konfiguration Ihres Anbieters überprüfen. Dazu muss überprüft werden, ob alle eigenschaften, die für den vollständigen Betrieb erforderlich sind, ordnungsgemäß festgelegt sind. Jeder Anbieter benötigt eine andere Anzahl von Eigenschaften. die Konfiguration hängt von Ihrem Anbieter und dem Grad der Benutzerinteraktion ab, die Sie zulassen. Einige Dienstanbieter behalten alle erforderlichen Eigenschaften im Profil bei. 

Andere Dienstanbieter behalten einen Teilsatz von Eigenschaften im Profil bei und fordert den Benutzer auf, fehlende Werte zu erhalten. Andere Anbieter speichern jedoch keine Eigenschaften im Profil und verlassen sich darauf, dass der Benutzer alle für die Konfiguration erforderlichen Informationen zur Verfügung hat.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>So rufen Sie im Profil gespeicherte Eigenschaften ab
  
1. Rufen [Sie IMAPISupport::OpenProfileSection auf,](imapisupport-openprofilesection.md)und übergeben Sie die [MAPIUID](mapiuid.md) Ihres Anbieters als Eingabeparameter. 
    
2. Rufen Sie die [IMAPIProp::GetProps-](imapiprop-getprops.md) oder [IMAPIProp::GetPropList-Methoden](imapiprop-getproplist.md) des Profilabschnitts auf, um einzelne Eigenschaften oder eine Eigenschaftenliste abzurufen. 
    
### <a name="to-set-properties-from-user-information"></a>So legen Sie Eigenschaften aus Benutzerinformationen
  
Zeigen Sie ein Eigenschaftenblatt an, wenn MAPI kein Flag festgelegt hat, das die Anzeige verbietet. Die folgenden Flags deuten darauf hin, dass keine Benutzeroberfläche angezeigt werden kann.
  
|**Wert**|**Dienstanbieter**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Adressbuchanbieter  <br/> |
|LOGON_NO_DIALOG  <br/> |Transportanbieter  <br/> |
|MDB_NO_DIALOG  <br/> |Anbieter des Nachrichtenspeichers  <br/> |
   
Wenn Ihr Anbieter nicht alle Konfigurationseigenschaften im Profil gespeichert hat und eine Benutzerinteraktion erforderlich ist, und MAPI eines der Dialogfeldunterdrückungsflags an Ihre Anmeldemethode übergibt, geben Sie MAPI_E_UNCONFIGURED. Geben Sie diesen Fehler auch zurück, wenn das Dialogfeldunterdrückungsflag nicht festgelegt ist, der Benutzer jedoch nicht alle erforderlichen Informationen zur Verfügung stellt.
  
Wenn ihr Dienstanbieter seine Anmeldemethode mit MAPI_E_UNCONFIGURED, ruft MAPI ihre Einstiegspunktfunktion erneut auf. Wenn die Informationen beim zweiten Anruf nicht gespeichert werden können, wird die Sitzung möglicherweise beendet, je nachdem, wie wichtig Ihr Dienstanbieter ist. 
  
Die folgende Abbildung zeigt die logik, die für die Konfiguration in der Anmeldemethode des Dienstanbieters erforderlich ist. 
  
**Flussdiagramm für Konfigurationsüberprüfung**
  
![Flussdiagramm zur Konfigurationsprüfung](media/amapi_62.gif "Konfigurationsüberprüfungsflussdiagramm")
  
## <a name="see-also"></a>Siehe auch

- [Implementieren der Dienstanbieteranmeldung](implementing-service-provider-logon.md)

