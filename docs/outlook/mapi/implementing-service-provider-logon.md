---
title: Implementieren der Dienstanbieteranmeldung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5651ab674071b832eb14d2ca217bd8cf0fa90196
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575694"
---
# <a name="implementing-service-provider-logon"></a>Implementieren der Dienstanbieteranmeldung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI ruft eine Methode in Ihrem Anbieterobjekt auf, um den Anmeldevorgang mithilfe des Zeigers zu starten, den Sie von Ihrer Einstiegspunktfunktion zurückgeben. Die Methode variiert je nach Typ des Dienstanbieters wie folgt:
  
- [IABProvider::Anmeldung](iabprovider-logon.md) für Adressbuchanbieter 
    
- [IMSProvider::Anmeldung](imsprovider-logon.md) für Nachrichtenspeicheranbieter 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) für Transportanbieter 
    
Führen Sie die folgenden Aufgaben in der von Ihnen implementierten Anmeldemethode aus:
  
1. Erhöhen Sie die Referenzanzahl für das Supportobjekt, das als Eingabeparameter übergeben wird, indem Sie seine [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen. 
    
2. Rufen Sie die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) des Supportobjekts auf, um auf Ihren Profilabschnitt zuzugreifen. 
    
3. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Profilabschnitts auf, um die folgenden Eigenschaften festzulegen: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Versuchen Sie nicht, die **Eigenschaften PR_RESOURCE_FLAGS** oder **PR_PROVIDER_DLL_NAME** des Profilabschnitts festzulegen. Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
4. Überprüfen Sie, ob die für die Konfiguration benötigten Eigenschaften entweder im Profil gespeichert sind oder vom Benutzer zur Verfügung stehen. Weitere Informationen zum Überprüfen Ihrer Konfiguration finden Sie unter [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).
    
5. Rufen Sie die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) des Supportobjekts auf, um einen eindeutigen Bezeichner oder [MAPIUID](mapiuid.md)zu registrieren, wenn Ihr Anbieter ein Adressbuch- oder Nachrichtenspeicheranbieter ist. Transportanbieter registrieren **MAPIUID-Strukturen,** wenn MAPI ihre [IXPLogon::AddressTypes-Methode aufruft.](ixplogon-addresstypes.md) Weitere Informationen zum Registrieren einer **MAPIUID** finden Sie unter [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).
    
6. Instanziieren Sie ein Anmeldeobjekt, und geben Sie es mit einem der folgenden Werte zurück:
    
  - S_OK, um auf eine erfolgreiche Anmeldung hinzuweisen.
    
  - MAPI_E_UNCONFIGURED, um anzugeben, dass eine oder mehrere der Konfigurationseigenschaften nicht verfügbar waren.
    
  - MAPI_E_USER_CANCEL, um anzugeben, dass der Benutzer das Konfigurationsdialogfeld abgebrochen hat, sodass die Konfigurationseigenschaften nicht verfügbar sind.
    
  - MAPI_E_FAILONEPROVIDER, um anzugeben, dass Ihr Anbieter nicht konfiguriert werden konnte, die MAPI die Verwendung jedoch unabhängig davon zulassen sollte. Anmeldemethoden sollten diesen Wert zurückgeben, um einen nichtfatalen Fehler zu melden, z. B. wenn der Anbieter ein Kennwort benötigt und der Benutzer nicht dazu aufgefordert werden kann, da die Benutzeroberfläche deaktiviert ist. 
    
In der vorherigen Aufgabenliste wird eine Mindestimplementierung für eine Anmeldemethode eines Dienstanbieters beschrieben. Sie können bei Bedarf zusätzliche Funktionen hinzufügen. Einige Anbieter rufen beispielsweise [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) auf, um die Statustabelle in ihrer Anmeldemethode zu aktualisieren. 
  
> [!NOTE]
> Um die beste Leistung bei der Anmeldung zu erzielen, vermeiden Sie den Aufruf von [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) oder [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Bevor diese Aufrufe abgeschlossen werden können und die Steuerung an die Anmeldemethode zurückgegeben werden kann, muss der MAPI-Spooler gestartet werden. 
  
## <a name="see-also"></a>Siehe auch

- [Starten eines Dienstanbieters](starting-a-service-provider.md)

