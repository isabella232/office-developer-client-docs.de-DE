---
title: Implementieren einer Dienstanbieteranmeldung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb64f2780530fd30784bf9a9b197bcde205b4a5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792572"
---
# <a name="implementing-service-provider-logon"></a>Implementieren einer Dienstanbieteranmeldung

**Betrifft**: Outlook 
  
MAPI-Aufrufen eine Methode in Ihrem Anbieterobjekt Beginn des Anmeldevorgangs mithilfe des Mauszeigers, mit dem Sie von Ihrem Eintrag Point-Funktion zurückgegeben. Die Methode hängt wie folgt auf den Typ des vom-Dienstanbieter:
  
- [IABProvider::Logon](iabprovider-logon.md) für adressbuchanbietern implementierte 
    
- [IMSProvider::Logon](imsprovider-logon.md) für Nachricht-Anbieter 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) für Transportanbieter 
    
Führen Sie die folgenden Aufgaben in jegliches Logon-Methode, die Sie implementieren:
  
1. Erhöhen Sie die Anzahl der Verweise auf die Support-Objekt, das als Eingabeparameter übergeben wird, durch dessen [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) -Methode aufrufen. 
    
2. Rufen Sie die des Unterstützungsobjekts [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode zum Zugriff auf Ihr Profilabschnitt. 
    
3. Rufen Sie den Profilabschnitt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die folgenden Eigenschaften festlegen: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Versuchen Sie nicht den Profil Eigenschaften des Abschnitts **PR_RESOURCE_FLAGS** oder **PR_PROVIDER_DLL_NAME** festgelegt. Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
4. Überprüfen Sie, dass die Eigenschaften für die Konfiguration benötigten entweder im Profil gespeichert werden oder vom Benutzer verfügbar sind. Weitere Informationen zum Überprüfen der Konfigurations finden Sie unter [Überprüfen der Dienstkonfiguration Anbieter](verifying-service-provider-configuration.md).
    
5. Rufen Sie die Support-Objekt [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode, um eine eindeutige Kennung oder [MAPIUID](mapiuid.md), registrieren, wenn der Anbieter einen Address Book oder einer Nachricht-Anbieter ist. Transportanbieter registrieren **MAPIUID** Strukturen, wenn MAPI ihre [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufruft. Weitere Informationen zum Registrieren einer **MAPIUID**finden Sie unter [Registrieren Service Provider eindeutige Bezeichner](registering-service-provider-unique-identifiers.md).
    
6. Instanziieren Sie ein Objekt Anmeldung und mit einem der folgenden Werte zurück:
    
  - S_OK erfolgreichen Anmeldung an.
    
  - Um anzugeben, dass eine oder mehrere der die Konfigurationseigenschaften MAPI_E_UNCONFIGURED waren nicht verfügbar.
    
  - MAPI_E_USER_CANCEL, um anzugeben, dass der Benutzer das Dialogfeld Konfiguration abgebrochen verursacht Konfigurationseigenschaften nicht verfügbar zu sein.
    
  - MAPI_E_FAILONEPROVIDER, um anzugeben, dass der Anbieter nicht konfiguriert werden konnte, aber die MAPI, unabhängig davon verwendet werden dürfen. Anmeldemethoden sollte diesen Wert, um eine ein nicht schwerwiegender Fehler, beispielsweise wenn der Anbieter ist ein Kennwort erforderlich und kann nicht für sie Benutzer auffordern, da die Benutzeroberfläche deaktiviert ist melden zurückgegeben. 
    
Die obigen Liste der Vorgänge wird eine minimale Implementierung für eine Service Provider Logon-Methode beschrieben. Sie können zusätzliche Funktionen bei Bedarf einschließen. Einige Anbieter rufen beispielsweise [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) zum Aktualisieren der Tabelle "Status" in ihre Logon (Methode). 
  
> [!NOTE]
> Um bei der Anmeldung die beste Leistung zu erzielen, vermeiden Sie [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) oder [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)aufrufen. Bevor dieser Anrufe können und die Steuerung an Ihre Logon (Methode) zurück, muss die MAPI-Warteschlange gestartet werden. 
  
## <a name="see-also"></a>Siehe auch

- [Starten eines Dienstanbieters](starting-a-service-provider.md)

