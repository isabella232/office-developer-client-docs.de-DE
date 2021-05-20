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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439730"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="f64a1-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="f64a1-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="f64a1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f64a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f64a1-105">Zeigt ein Eigenschaftenblatt an, mit dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann Diese Methode wird in von MAPI implementierten Statusobjekten nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f64a1-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f64a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f64a1-106">Parameters</span></span>

 <span data-ttu-id="f64a1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f64a1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f64a1-108">[in] Ein Handle zum übergeordneten Fenster des Konfigurationseigenschaftsblatts.</span><span class="sxs-lookup"><span data-stu-id="f64a1-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="f64a1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f64a1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f64a1-110">[in] Eine Bitmaske mit Flags, die die Anzeige des Eigenschaftenblatts steuert.</span><span class="sxs-lookup"><span data-stu-id="f64a1-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="f64a1-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f64a1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f64a1-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="f64a1-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="f64a1-113">Schlägt vor, dass der Anbieter keine Benutzer zum Ändern von Konfigurationseigenschaften aktivieren sollte.</span><span class="sxs-lookup"><span data-stu-id="f64a1-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="f64a1-114">Dieses Flag ist nur ein Vorschlag. sie kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="f64a1-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f64a1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f64a1-115">Return value</span></span>

<span data-ttu-id="f64a1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f64a1-116">S_OK</span></span> 
  
> <span data-ttu-id="f64a1-117">Das Konfigurationseigenschaftsblatt wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f64a1-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="f64a1-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f64a1-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f64a1-119">Das status-Objekt unterstützt diese Methode nicht, wie durch das Fehlen des STATUS_SETTINGS_DIALOG-Flag in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f64a1-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f64a1-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f64a1-120">Remarks</span></span>

<span data-ttu-id="f64a1-121">Die **IMAPIStatus::SettingsDialog-Methode** zeigt ein Konfigurationseigenschaftsblatt an.</span><span class="sxs-lookup"><span data-stu-id="f64a1-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="f64a1-122">Alle Dienstanbieter sollten die **SettingsDialog-Methode** unterstützen, sie ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f64a1-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="f64a1-123">Dienstanbieter können eigene Eigenschaftenblätter implementieren oder die Implementierung verwenden, die in der [IMAPISupport::D oConfigPropsheet-Methode des Supportobjekts bereitgestellt](imapisupport-doconfigpropsheet.md) wird.</span><span class="sxs-lookup"><span data-stu-id="f64a1-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="f64a1-124">**DoConfigPropsheet erstellt** ein Eigenschaftenblatt mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f64a1-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f64a1-125">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="f64a1-125">Notes to implementers</span></span>

<span data-ttu-id="f64a1-126">Wenn ein Remotetransportanbieter über Einstellungen verfügt, sollte er die folgenden Schritte vornehmen:</span><span class="sxs-lookup"><span data-stu-id="f64a1-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="f64a1-127">Öffnen Sie den Profilabschnitt des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="f64a1-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="f64a1-128">Holen Sie sich die Eigenschafteneinstellungen des Transportanbieters aus dem Profil.</span><span class="sxs-lookup"><span data-stu-id="f64a1-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="f64a1-129">Zeigen Sie die Eigenschafteneinstellungen in einem Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="f64a1-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="f64a1-130">Wenn das Dialogfeld die Bearbeitung der Eigenschafteneinstellungen zulässt, überprüfen Sie, ob die neuen Einstellungen gültig sind, und speichern Sie sie wieder im Profilabschnitt des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="f64a1-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="f64a1-131">Geben S_OK oder Fehlerwerte zurück, die während der vorherigen Schritte zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f64a1-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="f64a1-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f64a1-132">Notes to callers</span></span>

<span data-ttu-id="f64a1-133">Sie können das über **SettingsDialog** angezeigte Eigenschaftenblatt verwenden, um eine Vielzahl von Aufgaben auszuführen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="f64a1-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="f64a1-134">Geben Sie einen Standardnachrichtenspeicher an.</span><span class="sxs-lookup"><span data-stu-id="f64a1-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="f64a1-135">Geben Sie einen Transportauftrag an.</span><span class="sxs-lookup"><span data-stu-id="f64a1-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="f64a1-136">Geben Sie einen Standard-Adressbuchcontainer für das Browsen an.</span><span class="sxs-lookup"><span data-stu-id="f64a1-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="f64a1-137">Geben Sie eine Suchreihenfolge zum Auflösen mehrdeutiger Namen an.</span><span class="sxs-lookup"><span data-stu-id="f64a1-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="f64a1-138">Geben Sie ein standardmäßiges persönliches Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="f64a1-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="f64a1-139">Dienstanbieter können Je nach Eigenschaft Eigenschaftenblätter implementieren, die schreibgeschützt oder eine Mischung aus Berechtigungen sind.</span><span class="sxs-lookup"><span data-stu-id="f64a1-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="f64a1-140">Dienstanbieter können unterschiedliche Berechtigungen für einzelne Eigenschaften implementieren, indem Sie Eigenschaftseinschränkungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="f64a1-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="f64a1-141">Der Standardmodus für Eigenschaftenblätter ist Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f64a1-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="f64a1-142">Sie können schreibgeschützte Eigenschaftenblätter anfordern, indem Sie UI_READONLY in Ihren Aufrufen von **SettingsDialog festlegen.**</span><span class="sxs-lookup"><span data-stu-id="f64a1-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="f64a1-143">Dienstanbieter, die schreibgeschützte Eigenschaftenblätter implementieren können, können dies tun.</span><span class="sxs-lookup"><span data-stu-id="f64a1-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="f64a1-144">Da einige Dienstanbieter den Standardmodus jedoch nicht außer Kraft setzen können, müssen Sie bereit sein, Eigenschaftenblätter eines der beiden Typen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="f64a1-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="f64a1-145">Da an diesem Vorgang immer eine Benutzeroberfläche beteiligt ist, sollten nur interaktive Clients **SettingsDialog aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="f64a1-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f64a1-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f64a1-146">See also</span></span>



[<span data-ttu-id="f64a1-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="f64a1-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="f64a1-148">PidTagResourceMethods (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f64a1-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="f64a1-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f64a1-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

