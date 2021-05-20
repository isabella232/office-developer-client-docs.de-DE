---
title: Abrufen der primären und Anbieteridentität
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430812"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="7d046-103">Abrufen der primären und Anbieteridentität</span><span class="sxs-lookup"><span data-stu-id="7d046-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="7d046-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d046-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d046-105">Dienstanbieter, in der Regel Adressbuchanbieter, haben die Möglichkeit, eine Identität zur Darstellung der Sitzung in einer Vielzahl von Situationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="7d046-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="7d046-106">Drei Eigenschaften beschreiben die Identität eines Anbieters:</span><span class="sxs-lookup"><span data-stu-id="7d046-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="7d046-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7d046-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="7d046-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7d046-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="7d046-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7d046-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="7d046-110">Diese Eigenschaften werden auf die Eintrags-ID, den Anzeigenamen und den Suchschlüssel des entsprechenden Identitätsobjekts festgelegt, bei dem es sich in der Regel um einen Messagingbenutzer handelt.</span><span class="sxs-lookup"><span data-stu-id="7d046-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="7d046-111">Anbieter, die eine Identität liefern, legen auch das STATUS_PRIMARY_IDENTITY in ihrer **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7d046-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7d046-112">Je nach Ihren Anforderungen können Sie die Identität eines bestimmten Anbieters oder die primäre Identität für die Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d046-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="7d046-113">Sie können die Identität eines Anbieters auch zu Anzeigezwecken oder zum Abrufen von Eigenschaften wie PR_RESOURCE_PATH **(** [PidTagResourcePath](pidtagresourcepath-canonical-property.md)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d046-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="7d046-114">**PR_RESOURCE_PATH** enthält , falls festgelegt, den Pfad zu Dateien, die vom Anbieter verwendet oder erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7d046-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="7d046-115">Rufen Sie **die PR_RESOURCE_PATH-Eigenschaft** für den Anbieter ab, der die primäre Identität anliefert, wenn Sie Dateien suchen möchten, die für den Benutzer der Sitzung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7d046-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="7d046-116">**So rufen Sie die Identität eines bestimmten Anbieters ab**</span><span class="sxs-lookup"><span data-stu-id="7d046-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="7d046-117">Rufen [Sie IMAPISession::GetStatusTable auf,](imapisession-getstatustable.md) um auf die Statustabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7d046-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="7d046-118">Erstellen Sie eine Einschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um der **spalte PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) mit dem Namen des angegebenen Anbieters zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7d046-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="7d046-119">Rufen [Sie IMAPITable::FindRow auf,](imapitable-findrow.md) um die Zeile des Anbieters zu finden.</span><span class="sxs-lookup"><span data-stu-id="7d046-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="7d046-120">Die Identität des Anbieters wird in der Spalte **PR_IDENTITY_ENTRYID** gespeichert, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7d046-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="7d046-121">**So rufen Sie die primäre Identität für eine Sitzung ab**</span><span class="sxs-lookup"><span data-stu-id="7d046-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="7d046-122">Rufen [Sie IMAPISession::QueryIdentity auf.](imapisession-queryidentity.md)</span><span class="sxs-lookup"><span data-stu-id="7d046-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="7d046-123">**QueryIdentity** basiert auf dem Vorhandensein des STATUS_PRIMARY_IDENTITY in der spalte **PR_RESOURCE_FLAGS** für eine der Zeilen in der Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="7d046-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="7d046-124">Wenn keine der Statuszeilen diesen Wert festgelegt hat, weist **QueryIdentity** dem ersten Dienstanbieter, der die drei Eigenschaften PR_IDENTITY, eine Identität zu.</span><span class="sxs-lookup"><span data-stu-id="7d046-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="7d046-125">Wenn kein Dienstanbieter eine Identität angibt, gibt **QueryIdentity** MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="7d046-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="7d046-126">In diesem Fall sollten Sie eine Zeichenzeichenfolge erstellen, um einen generischen Benutzer zu repräsentieren, der als primäre Identität dienen kann.</span><span class="sxs-lookup"><span data-stu-id="7d046-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="7d046-127">**So legen Sie die primäre Identität für eine Sitzung explizit**</span><span class="sxs-lookup"><span data-stu-id="7d046-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="7d046-128">Rufen [Sie IMsgServiceAdmin::SetPrimaryIdentity auf.](imsgserviceadmin-setprimaryidentity.md)</span><span class="sxs-lookup"><span data-stu-id="7d046-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="7d046-129">Übergeben Sie **die MAPIUID** für den Zieldienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="7d046-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

