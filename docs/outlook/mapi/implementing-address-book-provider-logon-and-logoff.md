---
title: Implementieren einer An- und Abmeldung für Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f26e7b7ec607c9714012870d5367a0e775c62f34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572102"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="fbcb5-103">Implementieren einer An- und Abmeldung für Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="fbcb5-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="fbcb5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbcb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbcb5-105">Von adressbuchanbietern implementierte Sitzung an- und Abmelden durch Implementierung die Methoden des unterstützen die [IABProvider: IUnknown](iabprovideriunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="fbcb5-106">Die ** IABProvider ** Schnittstelle erbt direkt von **IUnknown** und fügt nur zwei andere Methoden: **Anmelden** und **Herunterfahren**.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-106">The ** IABProvider ** interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="fbcb5-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="fbcb5-107">Logoff</span></span>

<span data-ttu-id="fbcb5-108">MAPI rufen Ihres Anbieters- [IABProvider::Logon](iabprovider-logon.md) -Methode am Anfang jeder Sitzung und Ihrem Anbieter zum aktuellen Profil hinzugefügt und der Client DR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="fbcb5-109">Wenn MAPI die **IABProvider::Logon** -Methode aufruft, beginnt der Adressbuchanbieter seine Anmeldevorgang.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="fbcb5-110">**Implementieren von IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="fbcb5-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="fbcb5-111">Initialisieren Sie die Ausgabe Parameter Zeiger MAPI übergeben.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="fbcb5-112">Rufen Sie die des Unterstützungsobjekts **IUnknown:: AddRef** -Methode zum erhöht den Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="fbcb5-113">Rufen Sie die des Unterstützungsobjekts [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode, um den Abschnitt des Profils zu öffnen, Konfigurationsinformationen zu Ihrem Anbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="fbcb5-114">Übergeben Sie für den Parameter _LpUID_ und das Flag MAPI_MODIFY NULL, wenn Sie Änderungen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="fbcb5-115">Rufen Sie den Profilabschnitt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaften, die vom Dienstanbieter für die Anmeldung an, wie der Name der Datentabelle Datei oder Datenbank muss.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="fbcb5-116">Prüfen Sie, ob die Eigenschaften aller verfügbar und gültig.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="fbcb5-117">Wenn erforderlichen und zulässigen, zeigt ein Dialogfeld, wenn der Benutzer aufgefordert, nehmen Sie Korrekturen oder ungültige oder fehlende Informationen Ergänzungen und rufen Sie den Profilabschnitt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um alle Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="fbcb5-118">Die allgemeinen Eigenschaften, die verfügbar sein sollten gehören:</span><span class="sxs-lookup"><span data-stu-id="fbcb5-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="fbcb5-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fbcb5-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="fbcb5-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fbcb5-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="fbcb5-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fbcb5-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="fbcb5-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fbcb5-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="fbcb5-123">Stellen Sie keine **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) oder **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fbcb5-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="fbcb5-124">Bei der Anmeldung sind diese Eigenschaften schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="fbcb5-125">Wenn eine oder mehrere Konfigurationseigenschaften verfügbar sind, ein Fehler auftritt, und der Wert MAPI_E_UNCONFIGURED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="fbcb5-126">Rufen Sie [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) zum Registrieren einer [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="fbcb5-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="fbcb5-127">Vom Dienstanbieter kann eine **MAPIUID** durch erstellen:</span><span class="sxs-lookup"><span data-stu-id="fbcb5-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="fbcb5-128">Aufrufen der [IMAPISupport::NewUID](imapisupport-newuid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="fbcb5-129">Aufrufen der generiert. EXE-Tool eine GUID definieren, die vom Dienstanbieter verwendet, um in einem der seine Headerdateien einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="fbcb5-130">Speichern Sie Sie bei Bedarf eine neu erstellte **MAPIUID** im aktuellen Profil durch Aufrufen der Benutzerprofildienst-Abschnitt ** IMAPIProp::SetProps ** Methode.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's ** IMAPIProp::SetProps ** method.</span></span> 
    
9. <span data-ttu-id="fbcb5-131">Version Abschnitts Profile durch die **IUnknown** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="fbcb5-132">Instanziieren Sie ein neues Anmeldung-Objekt, und legen Sie den Inhalt des Parameters _LppABLogon_ auf die Adresse des neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="fbcb5-133">Da es möglich, für die MAPI aufrufen, ist Ihr ** Anmeldung **-Methode mehrmals im Laufe einer Sitzung; es ist ratsam, diese Möglichkeit in der Implementierung unterstützen, durch die Möglichkeit zum Erstellen mehrerer Logon-Objekten und Nachverfolgen der jedes Objekt, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-133">Because it is possible for MAPI to call your ** Logon ** method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="fbcb5-134">Unterstützung für mehrere Aufrufe der **Anmeldung** ermöglicht einem Benutzer von einer Clientanwendung aus, beispielsweise zur Anmeldung bei einer Sitzung mit unterschiedlichen Identitäten oder die Übermittlung Ziele verwenden.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="fbcb5-135">**Beim Herunterfahren** wird aufgerufen, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="fbcb5-136">MAPI die Methode aufruft, [IABProvider::Shutdown](iabprovider-shutdown.md) als eine der letzten Aufgaben beteiligt einer Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="fbcb5-137">MAPI stellt aller Ihres Anbieters Logon-Objekten und, wenn der Anbieter dieser Anruf empfängt, kann vorausgesetzt, dass dies ist der letzte Aufruf, die, den es empfängt.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="fbcb5-138">Führen Sie in der Implementierung der **IABProvider::Shutdown**eine abschließende Bereinigung, die Sie der Meinung sind erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="fbcb5-139">Beispielsweise möglicherweise Ihres Anbieters **MAPIDeinitIdle** anrufen, wenn sie **MAPIInitIdle** verwenden Sie das Modul im Leerlauf während der Sitzung oder die **IUnknown** -Methode alle Objekte, die noch freigegeben werden muss, um aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="fbcb5-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="fbcb5-140">Wenn der Anbieter keine abschließende Bereinigung aufweist, kann die Implementierung einer einzelnen Codezeile bestehen:</span><span class="sxs-lookup"><span data-stu-id="fbcb5-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


