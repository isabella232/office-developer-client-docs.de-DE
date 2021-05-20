---
title: Implementieren der Anmeldung und Abmelden von Adressbuchanbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438736"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementieren der Anmeldung und Abmelden von Adressbuchanbietern

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter unterstützen die Sitzungsanmeldung und -abmelde durch Implementieren der Methoden der [IABProvider : IUnknown-Schnittstelle.](iabprovideriunknown.md) Die ** IABProvider ** -Schnittstelle erbt direkt von **IUnknown** und fügt nur zwei weitere Methoden hinzu: **Anmeldung** und **Herunterfahren**. 
  
## <a name="logoff"></a>Abmelden

MAPI wird die [IABProvider::Logon-Methode](iabprovider-logon.md) Ihres Anbieters zu Beginn jeder Sitzung und immer dann aufrufen, wenn Ihr Anbieter dem aktuellen Profil hinzugefügt wird und der Client eine dynamische Neukonfiguration unterstützt. Wenn MAPI die **IABProvider::Logon-Methode** aufruft, beginnt Ihr Adressbuchanbieter mit dem Anmeldevorgang. 
  
**So implementieren Sie IABProvider::Log**
  
1. Initialisieren Sie alle von MAPI übergebenen Ausgabeparameterzeiger. 
    
2. Rufen Sie die **IUnknown::AddRef-Methode** des Supportobjekts auf, um die Referenzanzahl zu erhöhen. 
    
3. Rufen Sie die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) des Supportobjekts auf, um den Abschnitt des Profils zu öffnen, das Konfigurationsinformationen zu Ihrem Anbieter enthält. Übergeben Sie NULL für den  _lpUID-Parameter_ und das MAPI_MODIFY, wenn Sie Änderungen vornehmen möchten. 
    
4. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Profilabschnitts auf, um die Eigenschaften abzurufen, die Ihr Anbieter für die Anmeldung benötigt, z. B. den Namen der Datendatei oder Datenbanktabelle. 
    
5. Überprüfen Sie, ob alle Eigenschaften verfügbar und gültig sind. Zeigen Sie bei Bedarf und zulässig ein Dialogfeld an, in dem der Benutzer aufgefordert wird, Korrekturen oder Ergänzungen ungültiger oder fehlender Informationen vorzunehmen, und rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Profilabschnitts auf, um Änderungen zu speichern. Zu den allgemeinen Eigenschaften, die verfügbar sein sollten, gehören: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Legen Sie keine **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) oder **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
6. Wenn eine oder mehrere Konfigurationseigenschaften nicht verfügbar sind, führen Sie einen Fehler aus, und geben Sie den Wert MAPI_E_UNCONFIGURED.
    
7. Rufen [Sie IMAPISupport::SetProviderUID auf,](imapisupport-setprovideruid.md) um eine [MAPIUID zu registrieren.](mapiuid.md) Ihr Anbieter kann eine **MAPIUID durch** Folgendes erstellen: 
    
   - Aufrufen der [IMAPISupport::NewUID-Methode.](imapisupport-newuid.md) 
    
   - Aufrufen des UUIDGEN.EXE, um eine GUID zu definieren, die ihr Anbieter verwendet, um eine seiner Headerdateien zu verwenden.
    
8. Speichern Sie bei Bedarf eine neu erstellte **MAPIUID** im aktuellen Profil, indem Sie die ** IMAPIProp::SetProps **-Methode des Profilabschnitts aufrufen. 
    
9. Geben Sie den Profilabschnitt frei, indem Sie die **IUnknown::Release-Methode** aufrufen. 
    
10. Instanziieren Sie ein neues Anmeldeobjekt, und legen Sie den Inhalt des  _lppABLogon-Parameters_ auf die Adresse dieses neuen Objekts. 
    
Da MAPI ihre ** Logon **-Methode während einer Sitzung mehrmals aufrufen kann, ist es ratsam, diese Möglichkeit in Ihrer Implementierung zu unterstützen, indem sie mehrere Anmeldeobjekte erstellen und jedes erstellte Objekt nachverfolgen kann. Durch die **Unterstützung mehrerer Anmeldeaufrufe** kann sich ein Benutzer einer Clientanwendung beispielsweise bei einer Sitzung mit unterschiedlichen Identitäten anmelden oder unterschiedliche Zustellungsziele verwenden. 
  
**Das** Herunterfahren wird aufgerufen, wenn die Sitzung beendet wird. MAPI ruft Ihre [IABProvider::Shutdown-Methode](iabprovider-shutdown.md) als eine der letzten Aufgaben beim Herunterfahren einer Sitzung auf. MAPI hat alle Anmeldeobjekte Ihres Anbieters freigegeben, und wenn Ihr Anbieter diesen Anruf empfängt, kann davon ausgegangen werden, dass dies der letzte Anruf ist, den er erhält. Führen Sie in Ihrer Implementierung von **IABProvider::Shutdown** alle endgültigen Bereinigungen durch, die Sie für erforderlich halten. Ihr Anbieter kann z. B. **MAPIDeinitIdle** aufrufen, wenn **er MAPIInitIdle** aufgerufen hat, um das Leerlaufmodul während der Sitzung oder die **IUnknown::Release-Methode** aller Objekte zu verwenden, die noch freigegeben werden müssen. 
  
Wenn Ihr Anbieter keine endgültige Bereinigung hat, kann die Implementierung aus einer einzigen Codezeile besteht: 
  
```cpp
return S_OK;

```


