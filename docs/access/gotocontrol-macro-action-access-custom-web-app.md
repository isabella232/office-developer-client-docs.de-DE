---
title: GeheZuSteuerelement-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Mit der GeheZuSteuerelement-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht verschieben.
ms.openlocfilehash: 2368933a6277615554a565d3bdd973f7d1f366f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302576"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="3e029-103">GeheZuSteuerelement-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="3e029-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="3e029-104">Mit der **GeheZuSteuerelement**-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht verschieben.</span><span class="sxs-lookup"><span data-stu-id="3e029-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3e029-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="3e029-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="3e029-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="3e029-107">Setting</span></span>

<span data-ttu-id="3e029-108">Die **GeheZuSteuerelement**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="3e029-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="3e029-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="3e029-109">**Action argument**</span></span>|<span data-ttu-id="3e029-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e029-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e029-111">**Steuerelementname**</span><span class="sxs-lookup"><span data-stu-id="3e029-111">**Control Name**</span></span> <br/> |<span data-ttu-id="3e029-112">Der Name des Felds oder Steuerelements, das den Fokus erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="3e029-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="3e029-113">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="3e029-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e029-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e029-114">Remarks</span></span>

<span data-ttu-id="3e029-115">Sie können diese Aktion verwenden, wenn ein bestimmtes Feld oder Steuerelement den Fokus haben soll.</span><span class="sxs-lookup"><span data-stu-id="3e029-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="3e029-116">Sie können die Aktion auch zum Navigieren in einem Formular basierend auf bestimmten Bedingungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e029-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="3e029-117">Wenn der Benutzer z. B. im Steuerelement „Verheiratet“ auf einem Versicherungsformular „Nein“ angibt, kann der Fokus automatisch das Steuerelement „Name des Partners/der Partnerin“ überspringen und zum nächsten Steuerelement wechseln.</span><span class="sxs-lookup"><span data-stu-id="3e029-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

