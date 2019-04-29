---
title: Implementieren der Anmeldung und abMeldung des Adressbuch Anbieters
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
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementieren der Anmeldung und abMeldung des Adressbuch Anbieters

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter unterstützen die Sitzungs Anmeldung und-Abmeldung, indem Sie die Methoden der [IABProvider: IUnknown](iabprovideriunknown.md) -Schnittstelle implementieren. Die * * IABProvider * *-Schnittstelle erbt direkt von **IUnknown** und fügt nur zwei weitere Methoden hinzu: **Anmelden** und **Herunterfahren**. 
  
## <a name="logoff"></a>Abmelden

MAPI Ruft die [IABProvider:: LOGON](iabprovider-logon.md) -Methode Ihres Anbieters zu Beginn jeder Sitzung und immer dann auf, wenn der Anbieter dem aktuellen Profil hinzugefügt wird und der Client die dynamische Neukonfiguration unterstützt. Wenn MAPI die **IABProvider:: LOGON** -Methode aufruft, beginnt der Anmeldeprozess des Adressbuch Anbieters. 
  
**So implementieren Sie IABProvider:: Log**
  
1. Initialisieren Sie alle Ausgabeparameter Zeiger, die von MAPI übergeben wurden. 
    
2. Rufen Sie die **IUnknown:: AddRef** -Methode des Support Objekts auf, um den Verweiszähler zu erhöhen. 
    
3. Rufen Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode des Support Objekts auf, um den Abschnitt des Profils zu öffnen, das Konfigurationsinformationen zu Ihrem Anbieter enthält. Übergeben Sie NULL für den _lpUID_ -Parameter und das MAPI_MODIFY-Flag, wenn Sie Änderungen vornehmen möchten. 
    
4. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des profile-Abschnitts auf, um die Eigenschaften abzurufen, die der Anbieter für die Anmeldung benötigt, beispielsweise den Namen der Datendatei oder Datenbanktabelle. 
    
5. Überprüfen Sie, ob die Eigenschaften alle verfügbar und gültig sind. Wenn erforderlich und zulässig, zeigen Sie ein Dialogfeld an, in dem der Benutzer aufgefordert wird, Korrekturen oder Ergänzungen an ungültigen oder fehlenden Informationen vorzunehmen und die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Profil Abschnitts aufzurufen, um alle Änderungen zu speichern. Einige der allgemeinen Eigenschaften, die verfügbar sein sollten, sind: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Legen Sie **PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md)) oder **PR_PROVIDER_DLL_NAME** ([pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md)) nicht fest. Bei der Anmeldung sind diese Eigenschaften schreibgeschützt. 
  
6. Wenn mindestens eine Konfigurationseigenschaft nicht verfügbar ist, schlagen Sie fehl, und geben Sie den Wert MAPI_E_UNCONFIGURED zurück.
    
7. Rufen Sie [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) auf, um ein [MAPIUID](mapiuid.md)zu registrieren. Ihr Anbieter kann eine **MAPIUID** erstellen, indem Sie: 
    
   - Aufrufen der [IMAPISupport:: NewUID](imapisupport-newuid.md) -Methode. 
    
   - Aufrufen der UUIDGEN. EXE, um eine GUID zu definieren, die der Anbieter verwendet, um eine der Headerdateien einzuschließen.
    
8. Speichern Sie, falls gewünscht, eine neu erstellte **MAPIUID** im aktuellen Profil, indem Sie die * * IMAPIProp:: SetProps * *-Methode des profile-Abschnitts aufrufen. 
    
9. Geben Sie den Profil Abschnitt durch Aufrufen der **IUnknown:: Release** -Methode frei. 
    
10. Instanziieren Sie ein neues LOGON-Objekt, und legen Sie den Inhalt des _lppABLogon_ -Parameters auf die Adresse dieses neuen Objekts fest. 
    
Da MAPI die * * Logon * *-Methode während einer Sitzung mehrmals aufrufen kann, ist es ratsam, diese Möglichkeit in ihrer Implementierung zu unterstützen, indem Sie mehrere Anmeldeobjekte erstellen und alle erstellten Objekte nachverfolgen können. Durch die Unterstützung mehrerer **Anmelde** Aufrufe kann sich ein Benutzer einer Clientanwendung beispielsweise bei einer Sitzung mit unterschiedlichen Identitäten anmelden oder verschiedene Zusteller verwenden. 
  
Das **Herunterfahren** wird aufgerufen, wenn die Sitzung beendet wird. MAPI ruft Ihre [IABProvider:: Shutdown](iabprovider-shutdown.md) -Methode als eine der letzten Aufgaben beim Herunterfahren einer Sitzung auf. MAPI hat alle Anmeldeobjekte Ihres Anbieters freigegeben, und wenn Ihr Anbieter diesen Aufruf empfängt, kann davon ausgegangen werden, dass dies der letzte Anruf ist, den es empfängt. Führen Sie in ihrer Implementierung von **IABProvider:: Shutdown**eine abschließende Bereinigung durch, die Sie für erforderlich halten. Beispielsweise kann Ihr Anbieter **MAPIDeinitIdle** aufrufen, wenn es **MAPIInitIdle** aufgerufen hat, um das Leerlauf Modul während der Sitzung oder die **IUnknown:: Release** -Methode aller Objekte zu verwenden, die noch nicht freigegeben werden müssen. 
  
Wenn Ihr Anbieter keine abschließende Bereinigung aufweist, kann die Implementierung aus einer einzigen Codezeile bestehen: 
  
```cpp
return S_OK;

```


