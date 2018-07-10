---
title: Auslösenfehler-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: Die Auslösenfehler-Aktion zeigt ein Popupfenster, das eine angegebene Fehlermeldung enthält.
ms.openlocfilehash: 1176804106c5cfd9d4bd30f79f47975593089dbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790344"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="15896-103">Auslösenfehler-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="15896-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="15896-104">Die **Auslösenfehler** -Aktion zeigt ein Popupfenster, das eine angegebene Fehlermeldung enthält.</span><span class="sxs-lookup"><span data-stu-id="15896-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="15896-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="15896-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="15896-107">Die **AuslösenFehler** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15896-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="15896-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="15896-108">Setting</span></span>

<span data-ttu-id="15896-109">Die **Auslösenfehler** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="15896-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="15896-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="15896-110">**Argument**</span></span>|<span data-ttu-id="15896-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15896-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="15896-112">_Beschreibung des Fehlers_</span><span class="sxs-lookup"><span data-stu-id="15896-112">_Error Description_</span></span> <br/> |<span data-ttu-id="15896-113">Ein Zeichenfolgenausdruck, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="15896-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15896-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15896-114">Remarks</span></span>

<span data-ttu-id="15896-115">Wenn die **Auslösenfehler** -Aktion aufgerufen wird, werden alle Vorgänge in die aktuelle Transaktion rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="15896-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

