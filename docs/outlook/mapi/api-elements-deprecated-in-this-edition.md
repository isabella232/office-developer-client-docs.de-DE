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
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436888"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="34773-103">In dieser Edition veraltete API-Elemente</span><span class="sxs-lookup"><span data-stu-id="34773-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="34773-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34773-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34773-105">Die folgenden API-Elemente sind in der Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="34773-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="34773-106">Sie werden nicht mehr unterstützt, und Sie sollten sie nicht in neuen Projekten verwenden.</span><span class="sxs-lookup"><span data-stu-id="34773-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="34773-107">Veraltete Nachrichten- und Empfängeroptionen</span><span class="sxs-lookup"><span data-stu-id="34773-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="34773-108">Die folgenden API-Elemente sind in dieser Version aufgrund veralteter Nachrichten- und Empfängeroptionen veraltet:</span><span class="sxs-lookup"><span data-stu-id="34773-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="34773-109">**IXPLogon::RegisterOptions**– Das MAPI-Subsystem ruft diese Methode nicht mehr auf, um Standardwerte für Nachrichten- und Empfängeroptionen für einen Transportanbieter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34773-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="34773-110">**OPTIONDATA**– Diese Datenstruktur, die Eigenschaften für Nachrichten- und Empfängeroptionen unterstützt, ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="34773-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="34773-111">Das MAPI-Subsystem ruft **IXPLogon::RegisterOptions** nicht mehr auf, um Nachrichten- oder Empfängeroptionen zu erhalten, die ein Transportanbieter für einen bestimmten Adresstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34773-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="34773-112">**OPTIONCALLBACK**– Dieser Funktionsprototyp, den ein Transportanbieter zum Deklarieren einer Rückruffunktion verwendet hat und der wiederum das ZUM Auflösen der Eigenschaften des Anbieters verwendete MAPI-Subsystem ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="34773-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="34773-113">Das MAPI-Subsystem ruft nicht mehr **IXPLogon::RegisterOptions auf** oder verwendet eine rückruffunktion, die vom Transportanbieter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="34773-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="34773-114">**IMAPISession::MessageOptions**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzern das Festlegen von Eigenschaften zu ermöglichen, die einen bestimmten Nachrichten- und Adresstyp steuern.</span><span class="sxs-lookup"><span data-stu-id="34773-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="34773-115">Die Methode gibt immer MAPI_E_NOT_FOUND zurück, was angibt, dass es keine Nachrichtenoptionen für die bestimmte Nachricht gibt.</span><span class="sxs-lookup"><span data-stu-id="34773-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="34773-116">**IMAPISession::QueryDefaultMessageOpt**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Nachrichtenoptionen für einen bestimmten Adresstyp steuern.</span><span class="sxs-lookup"><span data-stu-id="34773-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="34773-117">Die Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.</span><span class="sxs-lookup"><span data-stu-id="34773-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="34773-118">**IAddrBook::RecipOptions**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzern das Festlegen von Eigenschaften zu ermöglichen, die die Verarbeitung für einen Empfänger eines bestimmten Adresstyps steuern.</span><span class="sxs-lookup"><span data-stu-id="34773-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="34773-119">Die Methode gibt immer MAPI_W_ERRORS_RETURNED zurück, was angibt, dass es keine Empfängeroptionen für den jeweiligen Empfänger gibt.</span><span class="sxs-lookup"><span data-stu-id="34773-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="34773-120">**IAddrBook::QueryDefaultRecipOpt**– MAPI-Client- und -Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Empfängeroptionen für einen bestimmten Adresstyp steuern.</span><span class="sxs-lookup"><span data-stu-id="34773-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="34773-121">Die Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.</span><span class="sxs-lookup"><span data-stu-id="34773-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34773-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34773-122">See also</span></span>



[<span data-ttu-id="34773-123">Erste Schritte mit der Outlook-MAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="34773-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

