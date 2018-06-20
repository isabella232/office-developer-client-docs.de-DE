---
title: In dieser Edition veraltete API-Elemente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: c70e89efba585183d2019bbda49102ecd14b9e20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791299"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="7b93d-103">In dieser Edition veraltete API-Elemente</span><span class="sxs-lookup"><span data-stu-id="7b93d-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="7b93d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b93d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b93d-105">Die folgenden API-Elemente sind in Microsoft Outlook 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="7b93d-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="7b93d-106">Sie werden nicht mehr unterstützt und sollten sie in neuen Projekten nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b93d-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="7b93d-107">Das Verwerfen der Nachricht sowie die Optionen für Empfänger</span><span class="sxs-lookup"><span data-stu-id="7b93d-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="7b93d-108">Die folgenden API-Elemente sind in dieser Version veraltet, da Sie veraltet Nachrichten- und Optionen:</span><span class="sxs-lookup"><span data-stu-id="7b93d-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="7b93d-109">**IXPLogon::RegisterOptions**– das MAPI-Subsystems nicht mehr diese Methode aufgerufen, um alle Standardwerte für Nachrichten und Empfänger Optionen für eine Adressbuchhierarchie herzustellen.</span><span class="sxs-lookup"><span data-stu-id="7b93d-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="7b93d-110">**OPTIONDATENQUELLE**– diese Datenstruktur, die Eigenschaften für die Nachricht und Empfänger unterstützt ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="7b93d-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="7b93d-111">MAPI-Subsystems ruft nicht mehr **IXPLogon::RegisterOptions** erhalten alle Nachrichten oder Optionen, die für einen bestimmten Adresstyp ein Transportdienstes unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b93d-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="7b93d-112">**OPTIONCALLBACK**– diese Funktionsprototyp ein Transportdienstes verwendet, um eine Callback-Funktion und, die wiederum Deklarieren des MAPI-Subsystems verwendet, um die Eigenschaften des Anbieters, Auflösen veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="7b93d-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="7b93d-113">MAPI-Subsystems nicht mehr aufruft **IXPLogon::RegisterOptions** oder eine beliebige der Adressbuchhierarchie zurückgegebene Callback-Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b93d-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="7b93d-114">**IMAPISession::MessageOptions**– MAPI-Client und Dienst Anbieter sollte diese Methode, um Eigenschaften anzuzeigen oder Benutzer Eigenschaften festlegen, die eine bestimmte Nachricht und Adresse Art steuern können nicht mehr aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7b93d-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="7b93d-115">Die Methode gibt immer MAPI_E_NOT_FOUND, die angibt, dass keine Nachrichtenoptionen für bestimmte Nachricht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7b93d-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="7b93d-116">**IMAPISession::QueryDefaultMessageOpt**– MAPI-Client und Dienst Anbieter sollte nicht mehr Aufrufen dieser Methode zum Abrufen von Eigenschaften, die für einen bestimmten Adresstyp Nachrichtenoptionen steuern.</span><span class="sxs-lookup"><span data-stu-id="7b93d-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="7b93d-117">Die Methode gibt einen Zeiger nicht mehr auf ein Array von Eigenschaftswerten.</span><span class="sxs-lookup"><span data-stu-id="7b93d-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="7b93d-118">**IAddrBook::RecipOptions**– MAPI-Client und Dienst Anbieter sollte diese Methode, um Eigenschaften anzuzeigen, oder lassen Benutzer legen Sie Eigenschaften, die diese Steuerelement Verarbeitung für einen Empfänger, der einen bestimmten Adresstyp nicht mehr aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7b93d-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="7b93d-119">Die Methode gibt immer MAPI_W_ERRORS_RETURNED, die angibt, dass es keine Empfänger Optionen für den bestimmten Empfänger sind.</span><span class="sxs-lookup"><span data-stu-id="7b93d-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="7b93d-120">**IAddrBook::QueryDefaultRecipOpt**– MAPI-Client und Dienst Anbieter sollte nicht mehr Aufrufen dieser Methode zum Abrufen von Eigenschaften, die Optionen für einen bestimmten Adresstyp steuern.</span><span class="sxs-lookup"><span data-stu-id="7b93d-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="7b93d-121">Die Methode gibt einen Zeiger nicht mehr auf ein Array von Eigenschaftswerten.</span><span class="sxs-lookup"><span data-stu-id="7b93d-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b93d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b93d-122">See also</span></span>



[<span data-ttu-id="7b93d-123">Erste Schritte mit der Outlook-MAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7b93d-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

