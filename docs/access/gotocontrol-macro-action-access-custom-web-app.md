---
title: GeheZuSteuerelement-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Die GeheZuSteuerelement-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790191"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="d2700-103">GeheZuSteuerelement-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="d2700-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d2700-104">Die **GeheZuSteuerelement** -Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="d2700-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d2700-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="d2700-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d2700-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d2700-107">Setting</span></span>

<span data-ttu-id="d2700-108">Die **GeheZuSteuerelement** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="d2700-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="d2700-109">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="d2700-109">**Action argument**</span></span>|<span data-ttu-id="d2700-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2700-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2700-111">**Steuerelementname**</span><span class="sxs-lookup"><span data-stu-id="d2700-111">**Control Name**</span></span> <br/> |<span data-ttu-id="d2700-112">Der Name des Felds oder Steuerelement den Fokus werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2700-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="d2700-113">Dabei handelt es sich um ein Pflichtargument.</span><span class="sxs-lookup"><span data-stu-id="d2700-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2700-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2700-114">Remarks</span></span>

<span data-ttu-id="d2700-115">Sie können diese Aktion verwenden, wenn Sie ein bestimmtes Feld oder Steuerelement den Fokus aufweisen soll.</span><span class="sxs-lookup"><span data-stu-id="d2700-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="d2700-116">Diese Aktion können auch um in einem Formular gemäß bestimmter Bedingungen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="d2700-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="d2700-117">Beispielsweise, wenn der Benutzer in einem Steuerelement Verheiratet No eingibt, kann der Fokus automatisch das Steuerelement Partner/in überspringen und zum nächsten Steuerelement zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d2700-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

