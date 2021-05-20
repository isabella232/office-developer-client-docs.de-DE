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
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="8130c-103">Implementieren der Anmeldung und Abmelden von Adressbuchanbietern</span><span class="sxs-lookup"><span data-stu-id="8130c-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="8130c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8130c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8130c-105">Adressbuchanbieter unterstützen die Sitzungsanmeldung und -abmelde durch Implementieren der Methoden der [IABProvider : IUnknown-Schnittstelle.](iabprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="8130c-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="8130c-106">Die \*\* IABProvider \*\* -Schnittstelle erbt direkt von **IUnknown** und fügt nur zwei weitere Methoden hinzu: **Anmeldung** und **Herunterfahren**.</span><span class="sxs-lookup"><span data-stu-id="8130c-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="8130c-107">Abmelden</span><span class="sxs-lookup"><span data-stu-id="8130c-107">Logoff</span></span>

<span data-ttu-id="8130c-108">MAPI wird die [IABProvider::Logon-Methode](iabprovider-logon.md) Ihres Anbieters zu Beginn jeder Sitzung und immer dann aufrufen, wenn Ihr Anbieter dem aktuellen Profil hinzugefügt wird und der Client eine dynamische Neukonfiguration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8130c-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="8130c-109">Wenn MAPI die **IABProvider::Logon-Methode** aufruft, beginnt Ihr Adressbuchanbieter mit dem Anmeldevorgang.</span><span class="sxs-lookup"><span data-stu-id="8130c-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="8130c-110">**So implementieren Sie IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="8130c-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="8130c-111">Initialisieren Sie alle von MAPI übergebenen Ausgabeparameterzeiger.</span><span class="sxs-lookup"><span data-stu-id="8130c-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="8130c-112">Rufen Sie die **IUnknown::AddRef-Methode** des Supportobjekts auf, um die Referenzanzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8130c-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="8130c-113">Rufen Sie die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) des Supportobjekts auf, um den Abschnitt des Profils zu öffnen, das Konfigurationsinformationen zu Ihrem Anbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="8130c-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="8130c-114">Übergeben Sie NULL für den  _lpUID-Parameter_ und das MAPI_MODIFY, wenn Sie Änderungen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="8130c-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="8130c-115">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Profilabschnitts auf, um die Eigenschaften abzurufen, die Ihr Anbieter für die Anmeldung benötigt, z. B. den Namen der Datendatei oder Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="8130c-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="8130c-116">Überprüfen Sie, ob alle Eigenschaften verfügbar und gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8130c-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="8130c-117">Zeigen Sie bei Bedarf und zulässig ein Dialogfeld an, in dem der Benutzer aufgefordert wird, Korrekturen oder Ergänzungen ungültiger oder fehlender Informationen vorzunehmen, und rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Profilabschnitts auf, um Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8130c-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="8130c-118">Zu den allgemeinen Eigenschaften, die verfügbar sein sollten, gehören:</span><span class="sxs-lookup"><span data-stu-id="8130c-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="8130c-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8130c-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="8130c-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8130c-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="8130c-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8130c-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="8130c-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8130c-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="8130c-123">Legen Sie keine **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) oder **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8130c-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="8130c-124">Bei der Anmeldung sind diese Eigenschaften schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8130c-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="8130c-125">Wenn eine oder mehrere Konfigurationseigenschaften nicht verfügbar sind, führen Sie einen Fehler aus, und geben Sie den Wert MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="8130c-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="8130c-126">Rufen [Sie IMAPISupport::SetProviderUID auf,](imapisupport-setprovideruid.md) um eine [MAPIUID zu registrieren.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="8130c-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="8130c-127">Ihr Anbieter kann eine **MAPIUID durch** Folgendes erstellen:</span><span class="sxs-lookup"><span data-stu-id="8130c-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="8130c-128">Aufrufen der [IMAPISupport::NewUID-Methode.](imapisupport-newuid.md)</span><span class="sxs-lookup"><span data-stu-id="8130c-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="8130c-129">Aufrufen des UUIDGEN.EXE, um eine GUID zu definieren, die ihr Anbieter verwendet, um eine seiner Headerdateien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8130c-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="8130c-130">Speichern Sie bei Bedarf eine neu erstellte **MAPIUID** im aktuellen Profil, indem Sie die \*\* IMAPIProp::SetProps \*\*-Methode des Profilabschnitts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8130c-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="8130c-131">Geben Sie den Profilabschnitt frei, indem Sie die **IUnknown::Release-Methode** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8130c-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="8130c-132">Instanziieren Sie ein neues Anmeldeobjekt, und legen Sie den Inhalt des  _lppABLogon-Parameters_ auf die Adresse dieses neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="8130c-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="8130c-133">Da MAPI ihre \*\* Logon \*\*-Methode während einer Sitzung mehrmals aufrufen kann, ist es ratsam, diese Möglichkeit in Ihrer Implementierung zu unterstützen, indem sie mehrere Anmeldeobjekte erstellen und jedes erstellte Objekt nachverfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="8130c-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="8130c-134">Durch die **Unterstützung mehrerer Anmeldeaufrufe** kann sich ein Benutzer einer Clientanwendung beispielsweise bei einer Sitzung mit unterschiedlichen Identitäten anmelden oder unterschiedliche Zustellungsziele verwenden.</span><span class="sxs-lookup"><span data-stu-id="8130c-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="8130c-135">**Das** Herunterfahren wird aufgerufen, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="8130c-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="8130c-136">MAPI ruft Ihre [IABProvider::Shutdown-Methode](iabprovider-shutdown.md) als eine der letzten Aufgaben beim Herunterfahren einer Sitzung auf.</span><span class="sxs-lookup"><span data-stu-id="8130c-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="8130c-137">MAPI hat alle Anmeldeobjekte Ihres Anbieters freigegeben, und wenn Ihr Anbieter diesen Anruf empfängt, kann davon ausgegangen werden, dass dies der letzte Anruf ist, den er erhält.</span><span class="sxs-lookup"><span data-stu-id="8130c-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="8130c-138">Führen Sie in Ihrer Implementierung von **IABProvider::Shutdown** alle endgültigen Bereinigungen durch, die Sie für erforderlich halten.</span><span class="sxs-lookup"><span data-stu-id="8130c-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="8130c-139">Ihr Anbieter kann z. B. **MAPIDeinitIdle** aufrufen, wenn **er MAPIInitIdle** aufgerufen hat, um das Leerlaufmodul während der Sitzung oder die **IUnknown::Release-Methode** aller Objekte zu verwenden, die noch freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8130c-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="8130c-140">Wenn Ihr Anbieter keine endgültige Bereinigung hat, kann die Implementierung aus einer einzigen Codezeile besteht:</span><span class="sxs-lookup"><span data-stu-id="8130c-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


