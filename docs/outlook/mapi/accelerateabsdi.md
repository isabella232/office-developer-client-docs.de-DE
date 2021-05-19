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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420374"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="9f258-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="9f258-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="9f258-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f258-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f258-105">Definiert eine Rückruffunktion zum Verarbeiten von Zugriffstasten in einem Dialogfeld ohne Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="9f258-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f258-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9f258-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f258-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f258-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9f258-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9f258-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="9f258-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f258-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f258-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="9f258-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="9f258-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="9f258-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="9f258-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f258-112">Parameters</span></span>

 <span data-ttu-id="9f258-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9f258-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="9f258-114">[in] Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f258-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="9f258-115">In Anwendungen, die unter Microsoft Windows ausgeführt werden, ist _ulUIParam_ das übergeordnete Fensterhandle für ein Dialogfeld und hat den Typ HWND, wird in ein ULONG_PTR **.**</span><span class="sxs-lookup"><span data-stu-id="9f258-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="9f258-116">Der Wert Null gibt an, dass kein übergeordnetes Fenster besteht.</span><span class="sxs-lookup"><span data-stu-id="9f258-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="9f258-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="9f258-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="9f258-118">[in] Zeiger auf eine Windows Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9f258-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f258-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f258-119">Return value</span></span>

<span data-ttu-id="9f258-120">Eine Funktion mit dem **ACCELERATEABSDI-Prototyp** gibt TRUE zurück, wenn sie die Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9f258-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9f258-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f258-121">Remarks</span></span>

<span data-ttu-id="9f258-122">Eine auf dem **ACCELERATEABSDI-Prototyp** basierende Funktion wird nur mit einem moduslosen Dialogfeld verwendet, d. h. nur, wenn die Clientanwendung das flag DIALOG_SDI im  _ulFlags-Element_ der [ADRPARM-Struktur](adrparm.md) festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="9f258-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="9f258-123">Ein modusloses Dialogfeld gibt die Nachrichtenschleife der Clientanwendung Windows, anstatt eine eigene Schleife zu haben.</span><span class="sxs-lookup"><span data-stu-id="9f258-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="9f258-124">Die Anwendung, die die Nachrichtenschleife steuert, weiß nicht, welche Zugriffstasten das Dialogfeld verwendet. Daher wird eine **ACCELERATEABSDI-basierte** Funktion aufgerufen, um Tastenkombinationen wie STRG+P zum Drucken zu testen und diese zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f258-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="9f258-125">Die Nachrichtenschleife eines Clients ruft die **ACCELERATEABSDI-basierte** Funktion auf, wenn der Client ein Dialogfeld ohne Adressbuch mit der [IAddrBook::Address-Methode](iaddrbook-address.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="9f258-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="9f258-126">Dieser Aufruf wird beendet, wenn MAPI eine Funktion aufruft, die auf dem [PROTOTYP der DISMISSMODELESS-Funktion](dismissmodeless.md) basiert.</span><span class="sxs-lookup"><span data-stu-id="9f258-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

