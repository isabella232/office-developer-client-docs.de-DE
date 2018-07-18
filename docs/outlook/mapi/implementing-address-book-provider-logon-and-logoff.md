---
title: Implementieren einer An- und Abmeldung für Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1ffde0814fe5024a3f89a93462c48136712f1013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792552"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementieren einer An- und Abmeldung für Adressbuchanbieter

**Betrifft**: Outlook 
  
Von adressbuchanbietern implementierte Sitzung an- und Abmelden durch Implementierung die Methoden des unterstützen die [IABProvider: IUnknown](iabprovideriunknown.md) Schnittstelle. Die ** IABProvider ** Schnittstelle erbt direkt von **IUnknown** und fügt nur zwei andere Methoden: **Anmelden** und **Herunterfahren**. 
  
## <a name="logoff"></a>Logoff

MAPI rufen Ihres Anbieters- [IABProvider::Logon](iabprovider-logon.md) -Methode am Anfang jeder Sitzung und Ihrem Anbieter zum aktuellen Profil hinzugefügt und der Client DR unterstützt. Wenn MAPI die **IABProvider::Logon** -Methode aufruft, beginnt der Adressbuchanbieter seine Anmeldevorgang. 
  
**Implementieren von IABProvider::Log**
  
1. Initialisieren Sie die Ausgabe Parameter Zeiger MAPI übergeben. 
    
2. Rufen Sie die des Unterstützungsobjekts **IUnknown:: AddRef** -Methode zum erhöht den Referenzzähler. 
    
3. Rufen Sie die des Unterstützungsobjekts [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode, um den Abschnitt des Profils zu öffnen, Konfigurationsinformationen zu Ihrem Anbieter enthält. Übergeben Sie für den Parameter _LpUID_ und das Flag MAPI_MODIFY NULL, wenn Sie Änderungen vornehmen möchten. 
    
4. Rufen Sie den Profilabschnitt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaften, die vom Dienstanbieter für die Anmeldung an, wie der Name der Datentabelle Datei oder Datenbank muss. 
    
5. Prüfen Sie, ob die Eigenschaften aller verfügbar und gültig. Wenn erforderlichen und zulässigen, zeigt ein Dialogfeld, wenn der Benutzer aufgefordert, nehmen Sie Korrekturen oder ungültige oder fehlende Informationen Ergänzungen und rufen Sie den Profilabschnitt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um alle Änderungen zu speichern. Die allgemeinen Eigenschaften, die verfügbar sein sollten gehören: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Stellen Sie keine **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) oder **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
6. Wenn eine oder mehrere Konfigurationseigenschaften verfügbar sind, ein Fehler auftritt, und der Wert MAPI_E_UNCONFIGURED zurückgegeben.
    
7. Rufen Sie [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) zum Registrieren einer [MAPIUID](mapiuid.md). Vom Dienstanbieter kann eine **MAPIUID** durch erstellen: 
    
   - Aufrufen der [IMAPISupport::NewUID](imapisupport-newuid.md) -Methode. 
    
   - Aufrufen der generiert. EXE-Tool eine GUID definieren, die vom Dienstanbieter verwendet, um in einem der seine Headerdateien einzuschließen.
    
8. Speichern Sie Sie bei Bedarf eine neu erstellte **MAPIUID** im aktuellen Profil durch Aufrufen der Benutzerprofildienst-Abschnitt ** IMAPIProp::SetProps ** Methode. 
    
9. Version Abschnitts Profile durch die **IUnknown** -Methode aufrufen. 
    
10. Instanziieren Sie ein neues Anmeldung-Objekt, und legen Sie den Inhalt des Parameters _LppABLogon_ auf die Adresse des neuen Objekts. 
    
Da es möglich, für die MAPI aufrufen, ist Ihr ** Anmeldung **-Methode mehrmals im Laufe einer Sitzung; es ist ratsam, diese Möglichkeit in der Implementierung unterstützen, durch die Möglichkeit zum Erstellen mehrerer Logon-Objekten und Nachverfolgen der jedes Objekt, das erstellt wird. Unterstützung für mehrere Aufrufe der **Anmeldung** ermöglicht einem Benutzer von einer Clientanwendung aus, beispielsweise zur Anmeldung bei einer Sitzung mit unterschiedlichen Identitäten oder die Übermittlung Ziele verwenden. 
  
**Beim Herunterfahren** wird aufgerufen, wenn die Sitzung beendet wird. MAPI die Methode aufruft, [IABProvider::Shutdown](iabprovider-shutdown.md) als eine der letzten Aufgaben beteiligt einer Sitzung beendet. MAPI stellt aller Ihres Anbieters Logon-Objekten und, wenn der Anbieter dieser Anruf empfängt, kann vorausgesetzt, dass dies ist der letzte Aufruf, die, den es empfängt. Führen Sie in der Implementierung der **IABProvider::Shutdown**eine abschließende Bereinigung, die Sie der Meinung sind erforderlich ist. Beispielsweise möglicherweise Ihres Anbieters **MAPIDeinitIdle** anrufen, wenn sie **MAPIInitIdle** verwenden Sie das Modul im Leerlauf während der Sitzung oder die **IUnknown** -Methode alle Objekte, die noch freigegeben werden muss, um aufgerufen wurde. 
  
Wenn der Anbieter keine abschließende Bereinigung aufweist, kann die Implementierung einer einzelnen Codezeile bestehen: 
  
```cpp
return S_OK;

```


