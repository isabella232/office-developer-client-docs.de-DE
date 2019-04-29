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
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="7a4b8-103">Implementieren der Anmeldung und abMeldung des Adressbuch Anbieters</span><span class="sxs-lookup"><span data-stu-id="7a4b8-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="7a4b8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a4b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a4b8-105">Adressbuchanbieter unterstützen die Sitzungs Anmeldung und-Abmeldung, indem Sie die Methoden der [IABProvider: IUnknown](iabprovideriunknown.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="7a4b8-106">Die \* \* IABProvider \* \*-Schnittstelle erbt direkt von **IUnknown** und fügt nur zwei weitere Methoden hinzu: **Anmelden** und **Herunterfahren**.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="7a4b8-107">Abmelden</span><span class="sxs-lookup"><span data-stu-id="7a4b8-107">Logoff</span></span>

<span data-ttu-id="7a4b8-108">MAPI Ruft die [IABProvider:: LOGON](iabprovider-logon.md) -Methode Ihres Anbieters zu Beginn jeder Sitzung und immer dann auf, wenn der Anbieter dem aktuellen Profil hinzugefügt wird und der Client die dynamische Neukonfiguration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="7a4b8-109">Wenn MAPI die **IABProvider:: LOGON** -Methode aufruft, beginnt der Anmeldeprozess des Adressbuch Anbieters.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="7a4b8-110">**So implementieren Sie IABProvider:: Log**</span><span class="sxs-lookup"><span data-stu-id="7a4b8-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="7a4b8-111">Initialisieren Sie alle Ausgabeparameter Zeiger, die von MAPI übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="7a4b8-112">Rufen Sie die **IUnknown:: AddRef** -Methode des Support Objekts auf, um den Verweiszähler zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="7a4b8-113">Rufen Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode des Support Objekts auf, um den Abschnitt des Profils zu öffnen, das Konfigurationsinformationen zu Ihrem Anbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="7a4b8-114">Übergeben Sie NULL für den _lpUID_ -Parameter und das MAPI_MODIFY-Flag, wenn Sie Änderungen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="7a4b8-115">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des profile-Abschnitts auf, um die Eigenschaften abzurufen, die der Anbieter für die Anmeldung benötigt, beispielsweise den Namen der Datendatei oder Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="7a4b8-116">Überprüfen Sie, ob die Eigenschaften alle verfügbar und gültig sind.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="7a4b8-117">Wenn erforderlich und zulässig, zeigen Sie ein Dialogfeld an, in dem der Benutzer aufgefordert wird, Korrekturen oder Ergänzungen an ungültigen oder fehlenden Informationen vorzunehmen und die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Profil Abschnitts aufzurufen, um alle Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="7a4b8-118">Einige der allgemeinen Eigenschaften, die verfügbar sein sollten, sind:</span><span class="sxs-lookup"><span data-stu-id="7a4b8-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="7a4b8-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a4b8-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="7a4b8-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a4b8-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="7a4b8-121">**PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a4b8-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="7a4b8-122">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a4b8-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="7a4b8-123">Legen Sie **PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md)) oder **PR_PROVIDER_DLL_NAME** ([pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md)) nicht fest.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="7a4b8-124">Bei der Anmeldung sind diese Eigenschaften schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="7a4b8-125">Wenn mindestens eine Konfigurationseigenschaft nicht verfügbar ist, schlagen Sie fehl, und geben Sie den Wert MAPI_E_UNCONFIGURED zurück.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="7a4b8-126">Rufen Sie [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) auf, um ein [MAPIUID](mapiuid.md)zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="7a4b8-127">Ihr Anbieter kann eine **MAPIUID** erstellen, indem Sie:</span><span class="sxs-lookup"><span data-stu-id="7a4b8-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="7a4b8-128">Aufrufen der [IMAPISupport:: NewUID](imapisupport-newuid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="7a4b8-129">Aufrufen der UUIDGEN. EXE, um eine GUID zu definieren, die der Anbieter verwendet, um eine der Headerdateien einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="7a4b8-130">Speichern Sie, falls gewünscht, eine neu erstellte **MAPIUID** im aktuellen Profil, indem Sie die \* \* IMAPIProp:: SetProps \* \*-Methode des profile-Abschnitts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="7a4b8-131">Geben Sie den Profil Abschnitt durch Aufrufen der **IUnknown:: Release** -Methode frei.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="7a4b8-132">Instanziieren Sie ein neues LOGON-Objekt, und legen Sie den Inhalt des _lppABLogon_ -Parameters auf die Adresse dieses neuen Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="7a4b8-133">Da MAPI die \* \* Logon \* \*-Methode während einer Sitzung mehrmals aufrufen kann, ist es ratsam, diese Möglichkeit in ihrer Implementierung zu unterstützen, indem Sie mehrere Anmeldeobjekte erstellen und alle erstellten Objekte nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="7a4b8-134">Durch die Unterstützung mehrerer **Anmelde** Aufrufe kann sich ein Benutzer einer Clientanwendung beispielsweise bei einer Sitzung mit unterschiedlichen Identitäten anmelden oder verschiedene Zusteller verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="7a4b8-135">Das **Herunterfahren** wird aufgerufen, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="7a4b8-136">MAPI ruft Ihre [IABProvider:: Shutdown](iabprovider-shutdown.md) -Methode als eine der letzten Aufgaben beim Herunterfahren einer Sitzung auf.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="7a4b8-137">MAPI hat alle Anmeldeobjekte Ihres Anbieters freigegeben, und wenn Ihr Anbieter diesen Aufruf empfängt, kann davon ausgegangen werden, dass dies der letzte Anruf ist, den es empfängt.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="7a4b8-138">Führen Sie in ihrer Implementierung von **IABProvider:: Shutdown**eine abschließende Bereinigung durch, die Sie für erforderlich halten.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="7a4b8-139">Beispielsweise kann Ihr Anbieter **MAPIDeinitIdle** aufrufen, wenn es **MAPIInitIdle** aufgerufen hat, um das Leerlauf Modul während der Sitzung oder die **IUnknown:: Release** -Methode aller Objekte zu verwenden, die noch nicht freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7a4b8-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="7a4b8-140">Wenn Ihr Anbieter keine abschließende Bereinigung aufweist, kann die Implementierung aus einer einzigen Codezeile bestehen:</span><span class="sxs-lookup"><span data-stu-id="7a4b8-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


