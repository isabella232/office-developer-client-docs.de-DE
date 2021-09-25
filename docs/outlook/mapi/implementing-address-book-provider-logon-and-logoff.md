---
title: Implementieren der Adressbuchanbieteranmeldung und -abmeldung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 863fc2caa7bbe3586ba0fb99ad705a95270abf4a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575673"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementieren der Adressbuchanbieteranmeldung und -abmeldung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter unterstützen die Sitzungsanmeldung und -abmeldung, indem die Methoden der [IABProvider : IUnknown-Schnittstelle](iabprovideriunknown.md) implementiert werden. Die ** IABProvider ** -Schnittstelle erbt direkt von **IUnknown** und fügt nur zwei andere Methoden hinzu: **Anmeldung** und **Herunterfahren.** 
  
## <a name="logoff"></a>Abmelden

Die MAPI ruft die [IABProvider::Logon-Methode](iabprovider-logon.md) Ihres Anbieters zu Beginn jeder Sitzung auf, und wenn Ihr Anbieter dem aktuellen Profil hinzugefügt wird und der Client die dynamische Neukonfiguration unterstützt. Wenn die MAPI die **IABProvider::Logon-Methode** aufruft, beginnt Ihr Adressbuchanbieter mit dem Anmeldevorgang. 
  
**So implementieren Sie IABProvider::Log**
  
1. Initialisieren Sie alle von mapi übergebenen Ausgabeparameterzeiger. 
    
2. Rufen Sie die **IUnknown::AddRef-Methode** des Supportobjekts auf, um die Referenzanzahl zu erhöhen. 
    
3. Rufen Sie die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) des Supportobjekts auf, um den Abschnitt des Profils zu öffnen, das Konfigurationsinformationen zu Ihrem Anbieter enthält. Übergeben Sie NULL für den  _Parameter lpUID_ und das flag MAPI_MODIFY, wenn Sie Änderungen vornehmen möchten. 
    
4. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Profilabschnitts auf, um die Eigenschaften abzurufen, die Ihr Anbieter für die Anmeldung benötigt, z. B. den Namen der Datendatei oder Datenbanktabelle. 
    
5. Überprüfen Sie, ob alle Eigenschaften verfügbar und gültig sind. Zeigen Sie ggf. ein Dialogfeld an, in dem der Benutzer aufgefordert wird, Korrekturen oder Ergänzungen zu ungültigen oder fehlenden Informationen vorzunehmen, und rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Profilabschnitts auf, um Änderungen zu speichern. Einige der allgemeinen Eigenschaften, die verfügbar sein sollten, sind: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Legen Sie **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) oder **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) nicht fest. Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
6. Wenn eine oder mehrere Konfigurationseigenschaften nicht verfügbar sind, schlagen Sie fehl, und geben Sie den Wert MAPI_E_UNCONFIGURED zurück.
    
7. Rufen Sie [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) auf, um eine [MAPIUID](mapiuid.md)zu registrieren. Ihr Anbieter kann eine **MAPIUID** wie folgt erstellen: 
    
   - Aufrufen der [IMAPISupport::NewUID-Methode.](imapisupport-newuid.md) 
    
   - Aufrufen des tools UUIDGEN.EXE, um eine GUID zu definieren, die ihr Anbieter verwendet, um sie in eine der Headerdateien einzuschließen.
    
8. Speichern Sie bei Bedarf eine neu erstellte **MAPIUID** im aktuellen Profil, indem Sie die ** IMAPIProp::SetProps ** -Methode des Profilabschnitts aufrufen. 
    
9. Geben Sie den Profilabschnitt frei, indem Sie die **IUnknown::Release-Methode** aufrufen. 
    
10. Instanziieren Sie ein neues Anmeldeobjekt, und legen Sie den Inhalt des  _lppABLogon-Parameters_ auf die Adresse dieses neuen Objekts fest. 
    
Da mapi Ihre ** Logon ** -Methode mehrmals während einer Sitzung aufrufen kann, empfiehlt es sich, diese Möglichkeit in Ihrer Implementierung zu unterstützen, indem Sie mehrere Anmeldeobjekte erstellen und jedes erstellte Objekt nachverfolgen können. Durch die Unterstützung mehrerer **Anmeldeaufrufe** kann sich ein Benutzer einer Clientanwendung beispielsweise bei einer Sitzung mit unterschiedlichen Identitäten anmelden oder unterschiedliche Zustellungsziele verwenden. 
  
**Das Herunterfahren** wird aufgerufen, wenn die Sitzung beendet wird. Die MAPI ruft Ihre [IABProvider::Shutdown-Methode](iabprovider-shutdown.md) als eine der letzten Aufgaben auf, die beim Herunterfahren einer Sitzung ausgeführt werden. Die MAPI hat alle Anmeldeobjekte Ihres Anbieters freigegeben, und wenn ihr Anbieter diesen Aufruf empfängt, kann er davon ausgehen, dass dies der letzte Anruf ist, den er erhält. Führen Sie in Ihrer Implementierung von **IABProvider::Shutdown** alle abschließenden Bereinigungen durch, die Ihrer Meinung nach erforderlich sind. Beispielsweise kann Ihr Anbieter **MAPIDeinitIdle** aufrufen, wenn **er MAPIInitIdle** aufgerufen hat, um das Leerlaufmodul während der Sitzung oder die **IUnknown::Release-Methode** aller Objekte zu verwenden, die noch nicht freigegeben werden müssen. 
  
Wenn Ihr Anbieter keine endgültige Bereinigung hat, kann die Implementierung aus einer einzelnen Codezeile bestehen: 
  
```cpp
return S_OK;

```


