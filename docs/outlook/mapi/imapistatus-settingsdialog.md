---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792341"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="50d38-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="50d38-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="50d38-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50d38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50d38-105">Zeigt ein Eigenschaftenfenster, in dem den Benutzer zum Ändern des Dienstanbieters Konfiguration dieser Methode wird nicht in Status-Objekten unterstützt, die MAPI implementiert.</span><span class="sxs-lookup"><span data-stu-id="50d38-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="50d38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50d38-106">Parameters</span></span>

 <span data-ttu-id="50d38-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="50d38-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="50d38-108">[in] Ein Handle für das übergeordnete Fenster im Eigenschaftsfenster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="50d38-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="50d38-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50d38-109">_ulFlags_</span></span>
  
> <span data-ttu-id="50d38-110">[in] Eine Bitmaske aus Flags, die die Anzeige des Eigenschaftenfensters steuert.</span><span class="sxs-lookup"><span data-stu-id="50d38-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="50d38-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="50d38-111">The following flag can be set:</span></span>
    
<span data-ttu-id="50d38-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="50d38-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="50d38-113">Impliziert, dass der Anbieter nicht Benutzer Konfigurationseigenschaften ändern kann sollen.</span><span class="sxs-lookup"><span data-stu-id="50d38-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="50d38-114">Dieses Kennzeichen ist nur ein Vorschlag. Es kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="50d38-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50d38-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="50d38-115">Return value</span></span>

<span data-ttu-id="50d38-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="50d38-116">S_OK</span></span> 
  
> <span data-ttu-id="50d38-117">Das Eigenschaftenblatt Konfiguration war erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50d38-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="50d38-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="50d38-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="50d38-119">Das Statusobjekt unterstützt diese Methode nicht, wie ohne das Flag STATUS_SETTINGS_DIALOG in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="50d38-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50d38-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50d38-120">Remarks</span></span>

<span data-ttu-id="50d38-121">**Die SettingsDialog** zeigt ein Eigenschaftenblatt Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="50d38-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="50d38-122">Alle-Dienstanbieter sollte die **SettingsDialog** -Methode unterstützt, aber es ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="50d38-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="50d38-123">Dienstanbieter können ihre eigenen Eigenschaftenseiten implementieren oder verwenden Sie die Implementierung [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) -Methode für die des Unterstützungsobjekts bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="50d38-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="50d38-124">**DoConfigPropsheet** erstellt ein Eigenschaftenblatt Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="50d38-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="50d38-125">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="50d38-125">Notes to implementers</span></span>

<span data-ttu-id="50d38-126">Weist ein remote-Transport-Anbieter auf eine beliebige Einstellung, sollten sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="50d38-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="50d38-127">Öffnen der Adressbuchhierarchie Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="50d38-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="50d38-128">Rufen Sie das Transportprotokoll eigenschafteneinstellungen des Anbieters aus dem Profil.</span><span class="sxs-lookup"><span data-stu-id="50d38-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="50d38-129">Anzeigen von Eigenschaften in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="50d38-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="50d38-130">Das Dialogfeld ermöglicht das Bearbeiten von Eigenschaften, sicher, dass die neuen Einstellungen gültig sind und in der Adressbuchhierarchie Profilabschnitt wieder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="50d38-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="50d38-131">Zurückgeben Sie S_OK oder während der vorherigen Schritte zurückgegebenen Fehlerwerte.</span><span class="sxs-lookup"><span data-stu-id="50d38-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="50d38-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="50d38-132">Notes to callers</span></span>

<span data-ttu-id="50d38-133">Das angezeigte über **SettingsDialog** Eigenschaftenblatt können Sie eine Vielzahl von Aufgaben wie die folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="50d38-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="50d38-134">Geben Sie einen Standard-Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="50d38-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="50d38-135">Geben Sie eine Transport-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="50d38-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="50d38-136">Geben Sie eine standardmäßige Adressbuchcontainer zum Durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="50d38-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="50d38-137">Geben Sie eine Suche Reihenfolge zum Auflösen von Namen nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="50d38-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="50d38-138">Geben Sie ein persönliches Standardadressbuch.</span><span class="sxs-lookup"><span data-stu-id="50d38-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="50d38-139">Dienstanbieter können implementieren, Eigenschaftenseiten, die Lese-/Schreibzugriff, schreibgeschützt sind oder eine Kombination von Berechtigungen, je nach Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="50d38-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="50d38-140">Dienstanbieter können unterschiedliche Berechtigungen für einzelne Eigenschaften implementieren, indem Sie Suchkriterien in Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="50d38-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="50d38-141">Der Standardmodus für Eigenschaftenseiten besteht Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="50d38-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="50d38-142">Sie können schreibgeschützte Eigenschaft Sheets anfordern, indem Sie das Flag UI_READONLY in Ihre Anrufe **SettingsDialog**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50d38-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="50d38-143">Dienstanbieter, die schreibgeschützte Eigenschaft Sheets implementieren können dazu.</span><span class="sxs-lookup"><span data-stu-id="50d38-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="50d38-144">Allerdings, da einige Dienstanbieter können Sie nicht den Standardmodus überschreiben, müssen Sie auf die Eigenschaftenseiten eines beliebigen Typs vorbereitet sein.</span><span class="sxs-lookup"><span data-stu-id="50d38-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="50d38-145">Da eine Benutzeroberfläche immer diesen Vorgang beteiligt ist, sollte nur interaktive Clients **SettingsDialog**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50d38-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50d38-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50d38-146">See also</span></span>



[<span data-ttu-id="50d38-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="50d38-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="50d38-148">Kanonische PidTagResourceMethods-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50d38-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="50d38-149">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="50d38-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

