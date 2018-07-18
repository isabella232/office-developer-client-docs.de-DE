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
ms.openlocfilehash: b7d4d758f7031c55aa3a23b662ec8727ea1e0719
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791247"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="01173-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="01173-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="01173-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01173-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01173-105">Definiert eine Callback-Funktion zum Prozess Zugriffstasten in ein Dialogfeld ohne Modus Address Book.</span><span class="sxs-lookup"><span data-stu-id="01173-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01173-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="01173-106">Header file:</span></span>  <br/> |<span data-ttu-id="01173-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01173-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="01173-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="01173-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="01173-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01173-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01173-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="01173-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="01173-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="01173-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="01173-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="01173-112">Parameters</span></span>

 <span data-ttu-id="01173-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="01173-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="01173-114">[in] Einen implementierungsspezifischen Wert für die Übergabe von Informationen zur Benutzeroberfläche auf eine Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="01173-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="01173-115">In Clientanwendungen unter Microsoft Windows _UlUIParam_ ist das übergeordnete Fensterhandle für ein Dialogfeld und vom Typ HWND in eine **ULONG_PTR**umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="01173-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="01173-116">Der Wert 0 gibt an, dass kein übergeordnetes Fenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="01173-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="01173-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="01173-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="01173-118">[in] Zeiger auf eine Windows-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="01173-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01173-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="01173-119">Return value</span></span>

<span data-ttu-id="01173-120">Eine Funktion mit dem Prototyp **ACCELERATEABSDI** gibt TRUE zurück, wenn die Meldung behandelt.</span><span class="sxs-lookup"><span data-stu-id="01173-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="01173-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01173-121">Remarks</span></span>

<span data-ttu-id="01173-122">Eine Funktion basierend auf den **ACCELERATEABSDI** Prototyp ist nur mit einem modalen Dialogfeld, d. h., nur verwendet, wenn die Clientanwendung das Flag DIALOG_SDI im _UlFlags_ -Member der [ADRPARM](adrparm.md) -Struktur eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="01173-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="01173-123">Nicht modales Dialogfeld teilt die Clientanwendung Windows Nachrichtenschleife, anstatt einen eigenen Schleife.</span><span class="sxs-lookup"><span data-stu-id="01173-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="01173-124">Die Anwendung, die die Nachrichtenschleife steuert, weiß nicht welche Zugriffstasten der Dialogfeld verwendet, damit es ein **ACCELERATEABSDI** aufruft, Grundlage Zugriffstasten wie STRG + P für den Druck Funktion zum Testen und fungieren.</span><span class="sxs-lookup"><span data-stu-id="01173-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="01173-125">Ein Client Nachricht Schleife Aufrufe der **ACCELERATEABSDI** basierend Funktion, wenn der Client einen nicht modalen Adressbücher in Dialogfeldern mit der [IAddrBook::Address](iaddrbook-address.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="01173-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="01173-126">In diesem Anruf wird beendet, wenn MAPI eine Funktion basierend auf den Prototyp [DISMISSMODELESS](dismissmodeless.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="01173-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

