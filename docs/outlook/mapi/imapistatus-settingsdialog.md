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
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="8c9ec-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="8c9ec-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="8c9ec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c9ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c9ec-105">Zeigt ein Eigenschaftenfenster an, in dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann diese Methode wird in den von MAPI implementierten Statusobjekten nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8c9ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c9ec-106">Parameters</span></span>

 <span data-ttu-id="8c9ec-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8c9ec-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8c9ec-108">in Ein Handle für das übergeordnete Fenster des Konfigurationseigenschaften Blatts.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="8c9ec-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8c9ec-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8c9ec-110">in Eine Bitmaske von Flags, die die Anzeige des Eigenschaftenblatts steuert.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="8c9ec-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8c9ec-111">The following flag can be set:</span></span>
    
<span data-ttu-id="8c9ec-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="8c9ec-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="8c9ec-113">Weist darauf hin, dass der Anbieter die Konfigurationseigenschaften nicht ändern sollte.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="8c9ec-114">Dieses Flag ist nur ein Vorschlag; Sie kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8c9ec-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c9ec-115">Return value</span></span>

<span data-ttu-id="8c9ec-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c9ec-116">S_OK</span></span> 
  
> <span data-ttu-id="8c9ec-117">Das Konfigurationseigenschaften Blatt wurde erfolgreich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="8c9ec-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8c9ec-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8c9ec-119">Das Status-Objekt unterstützt diese Methode nicht, wie durch das Fehlen des STATUS_SETTINGS_DIALOG-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c9ec-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c9ec-120">Remarks</span></span>

<span data-ttu-id="8c9ec-121">Die **IMAPIStatus:: Settingsdialog** -Methode zeigt ein Konfigurationseigenschaften Fenster an.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="8c9ec-122">Alle Dienstanbieter sollten die **Settingsdialog** -Methode unterstützen, Sie ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="8c9ec-123">Dienstanbieter können eigene Eigenschaftenblätter implementieren oder die Implementierung verwenden, die in der [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode des Support-Objekts bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="8c9ec-124">**DoConfigPropsheet** erstellt ein Eigenschaftenblatt mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8c9ec-125">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="8c9ec-125">Notes to implementers</span></span>

<span data-ttu-id="8c9ec-126">Wenn ein Remote Transportanbieter über Einstellungen verfügt, sollte er folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="8c9ec-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="8c9ec-127">Öffnen Sie den Abschnitt Profil des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="8c9ec-128">Rufen Sie die Eigenschafteneinstellungen des Transportanbieters aus dem Profil ab.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="8c9ec-129">Zeigen Sie die Eigenschafteneinstellungen in einem Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="8c9ec-130">Wenn im Dialogfeld die Eigenschafteneinstellungen bearbeitet werden können, überprüfen Sie, ob die neuen Einstellungen gültig sind, und speichern Sie Sie im Abschnitt Profil des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="8c9ec-131">Zurückgeben von S_OK oder von Fehlerwerten, die während der vorangehenden Schritte zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="8c9ec-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8c9ec-132">Notes to callers</span></span>

<span data-ttu-id="8c9ec-133">Mithilfe des Eigenschaftenblatts, das über **Settingsdialog** angezeigt wird, können Sie verschiedene Aufgaben ausführen, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="8c9ec-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="8c9ec-134">Angeben eines Standardnachrichten Speichers.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="8c9ec-135">Geben Sie einen Transportauftrag an.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="8c9ec-136">Geben Sie einen standardmäßigen Adressbuchcontainer für das Browsen an.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="8c9ec-137">Geben Sie eine Suchreihenfolge zum Auflösen von mehrdeutigen Namen an.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="8c9ec-138">Angeben eines standardmäßigen persönlichen Adressbuchs.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="8c9ec-139">Dienstanbieter können abhängig von der Eigenschaft Eigenschaftenblätter implementieren, die Lese-/Schreibzugriff, schreibgeschützt oder eine Kombination aus Berechtigungen sind.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="8c9ec-140">Dienstanbieter können unterschiedliche Berechtigungen für einzelne Eigenschaften implementieren, indem Sie Eigenschaftseinschränkungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="8c9ec-141">Der Standardmodus für Eigenschaftenblätter ist Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="8c9ec-142">Sie können schreibgeschützte Eigenschaftenblätter anfordern, indem Sie das UI_READONLY-Flag in ihren Aufrufen an **Settingsdialog**festlegen.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="8c9ec-143">Dienstanbieter, die schreibgeschützte Eigenschaftenblätter implementieren können, sind in der Lage, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="8c9ec-144">Da einige Dienstanbieter den Standardmodus jedoch nicht außer Kraft setzen können, müssen Sie bereit sein, Eigenschaftenblätter eines der beiden Typen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="8c9ec-145">Da eine Benutzeroberfläche immer an diesem Vorgang beteiligt ist, sollten nur interaktive Clients **Settingsdialog**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8c9ec-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c9ec-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c9ec-146">See also</span></span>



[<span data-ttu-id="8c9ec-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="8c9ec-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="8c9ec-148">Kanonische Pidtagresourcemethods (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c9ec-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="8c9ec-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8c9ec-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

