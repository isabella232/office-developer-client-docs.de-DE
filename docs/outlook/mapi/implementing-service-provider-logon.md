---
title: Implementieren der Dienstanbieteranmeldung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310087"
---
# <a name="implementing-service-provider-logon"></a>Implementieren der Dienstanbieteranmeldung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI ruft eine Methode in Ihrem Anbieterobjekt auf, um den Anmeldevorgang mithilfe des Zeigers zu beginnen, den Sie von Ihrer Einstiegspunktfunktion zurückgeben. Die Methode variiert je nach Typ Ihres Dienstanbieters wie folgt:
  
- [IABProvider::Anmeldung](iabprovider-logon.md) für Adressbuchanbieter 
    
- [IMSProvider::Anmeldung für](imsprovider-logon.md) Nachrichtenspeicheranbieter 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) für Transportanbieter 
    
Führen Sie die folgenden Aufgaben in der von Ihnen implementierten Anmeldemethode aus:
  
1. Erhöhen Sie die Referenzanzahl für das Supportobjekt, das als Eingabeparameter übergeben wird, indem Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen. 
    
2. Rufen Sie die [IMAPISupport::OpenProfileSection-Methode des Supportobjekts](imapisupport-openprofilesection.md) auf, um auf Ihren Profilabschnitt zu zugreifen. 
    
3. Rufen Sie die [IMAPIProp::SetProps-Methode des Profilabschnitts auf,](imapiprop-setprops.md) um die folgenden Eigenschaften zu setzen: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Versuchen Sie nicht, die Eigenschaften des **Profilabschnitts PR_RESOURCE_FLAGS** **PR_PROVIDER_DLL_NAME** festlegen. Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
4. Überprüfen Sie, ob die eigenschaften, die Sie für die Konfiguration benötigen, entweder im Profil gespeichert sind oder vom Benutzer verfügbar sind. Weitere Informationen zum Überprüfen der Konfiguration finden Sie unter [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).
    
5. Rufen Sie die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) des Supportobjekts auf, um einen eindeutigen Bezeichner oder [MAPIUID](mapiuid.md)zu registrieren, wenn Ihr Anbieter ein Adressbuch- oder Nachrichtenspeicheranbieter ist. Transportanbieter registrieren **MAPIUID-Strukturen,** wenn MAPI ihre [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) aufruft. Weitere Informationen zum Registrieren einer **MAPIUID finden** Sie unter [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).
    
6. Instanziieren Sie ein Anmeldeobjekt, und geben Sie einen der folgenden Werte zurück:
    
  - S_OK, um eine erfolgreiche Anmeldung anzugeben.
    
  - MAPI_E_UNCONFIGURED, dass mindestens eine der Konfigurationseigenschaften nicht verfügbar war.
    
  - MAPI_E_USER_CANCEL, dass der Benutzer das Konfigurationsdialogfeld abgebrochen hat, wodurch Konfigurationseigenschaften nicht verfügbar sind.
    
  - MAPI_E_FAILONEPROVIDER, dass Ihr Anbieter nicht konfiguriert werden konnte, dass MAPI die Verwendung jedoch unabhängig davon zulassen sollte. Anmeldemethoden sollten diesen Wert zurückgeben, um einen nicht standardmäßigen Fehler zu melden, z. B. wenn der Anbieter ein Kennwort benötigt und den Benutzer nicht dazu aufgefordert werden kann, da die Benutzeroberfläche deaktiviert ist. 
    
In der vorherigen Aufgabenliste wird eine Mindestimplementierung für eine Dienstanbieteranmeldungsmethode beschrieben. Sie können bei Bedarf zusätzliche Funktionen hinzufügen. Beispielsweise rufen einige Anbieter [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) auf, um die Statustabelle in ihrer Anmeldemethode zu aktualisieren. 
  
> [!NOTE]
> Um die beste Leistung bei der Anmeldung zu erzielen, vermeiden Sie den Aufruf von [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) oder [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Bevor diese Aufrufe abgeschlossen werden können und die Steuerung der Anmeldemethode zurückgeben kann, muss der MAPI-Spooler gestartet werden. 
  
## <a name="see-also"></a>Siehe auch

- [Starten eines Dienstanbieters](starting-a-service-provider.md)

