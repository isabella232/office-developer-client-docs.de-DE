---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322127"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="5b0f4-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="5b0f4-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="5b0f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b0f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b0f4-105">Definiert eine Rückruffunktion zum Verarbeiten von Zugriffstasten in einem nicht modalen Adressbuch Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b0f4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5b0f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="5b0f4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5b0f4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5b0f4-108">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5b0f4-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5b0f4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5b0f4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5b0f4-110">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5b0f4-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5b0f4-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5b0f4-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="5b0f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b0f4-112">Parameters</span></span>

 <span data-ttu-id="5b0f4-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5b0f4-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="5b0f4-114">in Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="5b0f4-115">In Anwendungen, die unter Microsoft Windows laufen, ist _ulUIParam_ das übergeordnete Fensterhandle für ein Dialogfeld und vom Typ HWND und wird in eine **ULONG_PTR**umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="5b0f4-116">Der Wert 0 (null) gibt an, dass kein übergeordnetes Fenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="5b0f4-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="5b0f4-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="5b0f4-118">in Zeiger auf eine Windows-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b0f4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b0f4-119">Return value</span></span>

<span data-ttu-id="5b0f4-120">Eine Funktion mit dem **ACCELERATEABSDI** -Prototyp gibt true zurück, wenn Sie die Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5b0f4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b0f4-121">Remarks</span></span>

<span data-ttu-id="5b0f4-122">Eine auf dem **ACCELERATEABSDI** -Prototyp basierende Funktion wird nur mit einem nicht modalen Dialogfeldverwendet, das heißt nur, wenn die Clientanwendung das DIALOG_SDI-Flag im _ulFlags_ -Element der [ADRPARM](adrparm.md) -Struktur festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="5b0f4-123">Ein nicht modales Dialogfeld teilt die Windows-Meldungsschleife der Clientanwendung, statt eine eigene Schleife zu haben.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="5b0f4-124">Die Anwendung, die die Nachrichtenschleife steuert, weiß nicht, welche Tastenkombinationen im Dialogfeldverwendet werden, und ruft daher eine **ACCELERATEABSDI** -basierte Funktion auf, um Zugriffstasten wie STRG + P zum Drucken zu testen und zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="5b0f4-125">Die Meldungsschleife eines Clients Ruft die **ACCELERATEABSDI** -basierte Funktion auf, wenn der Client ein nicht modales Adressbuch-Dialogfeld mit der [IAddrBook:: Address](iaddrbook-address.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="5b0f4-126">Dieser Aufruf wird beendet, wenn MAPI eine Funktion aufruft, die auf dem Prototyp der [DISMISSMODELESS](dismissmodeless.md) -Funktion basiert.</span><span class="sxs-lookup"><span data-stu-id="5b0f4-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

