---
title: Implementieren der Dienstanbieter Anmeldung
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
# <a name="implementing-service-provider-logon"></a>Implementieren der Dienstanbieter Anmeldung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI Ruft eine Methode in Ihrem Provider-Objekt auf, um den Anmeldevorgang mithilfe des Zeigers zu beginnen, den Sie von der Einstiegspunktfunktion zurückgeben. Je nach Typ des Dienstanbieters variiert die Methode wie folgt:
  
- [IABProvider:: Anmeldung](iabprovider-logon.md) für Adressbuchanbieter 
    
- [IMSProvider:: Anmeldung](imsprovider-logon.md) für Nachrichtenspeicher Anbieter 
    
- [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) für Transportanbieter 
    
Führen Sie die folgenden Aufgaben in der von Ihnen implementierten Anmeldemethode aus:
  
1. Inkrementieren Sie die Verweisanzahl für das Support Objekt, das als Eingabeparameter übergeben wird, indem Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode aufrufen. 
    
2. Rufen Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode des Support Objekts auf, um auf Ihren Profil Abschnitt zuzugreifen. 
    
3. Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des profile-Abschnitts auf, um die folgenden Eigenschaften festzulegen: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Versuchen Sie nicht, die **PR_RESOURCE_FLAGS** -oder **PR_PROVIDER_DLL_NAME** -Eigenschaften des profilbereichs festzulegen. Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
4. Stellen Sie sicher, dass die Eigenschaften, die Sie für die Konfiguration benötigen, entweder im Profil gespeichert sind oder vom Benutzer zur Verfügung stehen. Weitere Informationen zum Überprüfen der Konfiguration finden Sie unter [verifyIng Service Provider Configuration](verifying-service-provider-configuration.md).
    
5. Rufen Sie die [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode des Support Objekts auf, um einen eindeutigen Bezeichner oder [MAPIUID](mapiuid.md)zu registrieren, wenn es sich bei Ihrem Anbieter um ein Adressbuch oder einen Nachrichtenspeicher Anbieter handelt. Transport Anbieter registrieren **MAPIUID** -Strukturen, wenn MAPI Ihre [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode aufruft. Weitere Informationen zum Registrieren eines **MAPIUID**finden Sie unter [Registrieren von eindeutigen Bezeichnern des Dienstanbieters](registering-service-provider-unique-identifiers.md).
    
6. Instanziieren Sie ein LOGON-Objekt, und geben Sie mit einem der folgenden Werte zurück:
    
  - S_OK, um eine erfolgreiche Anmeldung anzuzeigen.
    
  - MAPI_E_UNCONFIGURED, um anzugeben, dass mindestens eine der Konfigurationseigenschaften nicht verfügbar war.
    
  - MAPI_E_USER_CANCEL, um anzugeben, dass der Benutzer das Konfigurationsdialogfeld abgebrochen hat, sodass die Konfigurationseigenschaften nicht verfügbar sind.
    
  - MAPI_E_FAILONEPROVIDER, um anzugeben, dass der Anbieter nicht konfiguriert werden konnte, dass MAPI jedoch unabhängig davon verwendet werden sollte. Anmeldemethoden sollten diesen Wert zurückgeben, um einen nicht schwerwiegenden Fehler zu melden, beispielsweise wenn der Anbieter ein Kennwort erfordert und den Benutzer nicht dazu auffordern kann, da die Benutzeroberfläche deaktiviert ist. 
    
Die vorangehende Aufgabenliste beschreibt eine Mindestimplementierung für eine Dienstanbieter-Anmeldemethode. Sie können bei Bedarf zusätzliche Funktionalitäten hinzufügen. Einige Anbieter rufen beispielsweise [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) auf, um die Statustabelle in ihrer Anmeldemethode zu aktualisieren. 
  
> [!NOTE]
> Um die beste Leistung zur Anmeldezeit zu erzielen, müssen Sie entweder [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) oder [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md)aufrufen. Bevor diese Aufrufe abgeschlossen und die Steuerung an Ihre Anmeldemethode zurückgegeben werden können, muss der MAPI-Spooler gestartet werden. 
  
## <a name="see-also"></a>Siehe auch

- [Starten eines Dienstanbieters](starting-a-service-provider.md)

