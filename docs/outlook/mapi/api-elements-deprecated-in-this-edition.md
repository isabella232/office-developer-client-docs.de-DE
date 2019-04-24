---
title: In dieser Edition deprecated API-Elemente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318207"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="d45ff-103">In dieser Edition deprecated API-Elemente</span><span class="sxs-lookup"><span data-stu-id="d45ff-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="d45ff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d45ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d45ff-105">Die folgenden API-Elemente sind in Microsoft Outlook 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="d45ff-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="d45ff-106">Sie werden nicht mehr unterstützt, und Sie sollten Sie nicht in neuen Projekten verwenden.</span><span class="sxs-lookup"><span data-stu-id="d45ff-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="d45ff-107">Veraltet Nachrichten-und Empfängeroptionen</span><span class="sxs-lookup"><span data-stu-id="d45ff-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="d45ff-108">Die folgenden API-Elemente sind in dieser Release aufgrund veralteter Nachrichten-und Empfängeroptionen veraltet:</span><span class="sxs-lookup"><span data-stu-id="d45ff-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="d45ff-109">**IXPLogon:: Register**Options – das MAPI-Subsystem ruft diese Methode nicht mehr auf, um Standardwerte für Nachrichten-und Empfängeroptionen für einen Transportanbieter einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d45ff-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="d45ff-110">**, OptionDatenquelle**– diese Datenstruktur, die Eigenschaften für Nachrichten-und Empfängeroptionen unterstützt hat, ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d45ff-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="d45ff-111">Das MAPI-Subsystem ruft **IXPLogon:: Register** options nicht mehr auf, um Nachrichten-oder Empfängeroptionen abzurufen, die ein Transportanbieter für einen bestimmten Adresstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d45ff-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="d45ff-112">**OPTIONCALLBACK**– dieser Funktionsprototyp, den ein Transportanbieter zum Deklarieren einer Rückruffunktion verwendet hat und der wiederum das MAPI-Subsystem zum Auflösen der Eigenschaften des Anbieters verwendet, ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d45ff-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="d45ff-113">Das MAPI-Subsystem ruft **IXPLogon:: registeroptions** nicht mehr auf oder verwendet eine Rückruffunktion, die vom Transportanbieter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d45ff-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="d45ff-114">**IMAPISession:: messageoptions**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzereigenschaften festzulegen, die eine bestimmte Nachricht und einen bestimmten Adresstyp steuern.</span><span class="sxs-lookup"><span data-stu-id="d45ff-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="d45ff-115">Die Methode gibt immer MAPI_E_NOT_FOUND zurück, was bedeutet, dass für die jeweilige Nachricht keine Nachrichtenoptionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d45ff-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="d45ff-116">**IMAPISession:: QueryDefaultMessageOpt**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Nachrichtenoptionen für einen bestimmten Adresstyp steuern.</span><span class="sxs-lookup"><span data-stu-id="d45ff-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="d45ff-117">Die-Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.</span><span class="sxs-lookup"><span data-stu-id="d45ff-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="d45ff-118">**IAddrBook:: RecipOptions**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften anzuzeigen oder Benutzereigenschaften festzulegen, die die Verarbeitung für einen Empfänger eines bestimmten Adresstyps steuern.</span><span class="sxs-lookup"><span data-stu-id="d45ff-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="d45ff-119">Die Methode gibt immer MAPI_W_ERRORS_RETURNED zurück, was bedeutet, dass für den jeweiligen Empfänger keine Empfängeroptionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d45ff-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="d45ff-120">**IAddrBook:: QueryDefaultRecipOpt**– MAPI-Client-und-Dienstanbieter sollten diese Methode nicht mehr aufrufen, um Eigenschaften abzurufen, die Empfängeroptionen für einen bestimmten Adresstyp steuern.</span><span class="sxs-lookup"><span data-stu-id="d45ff-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="d45ff-121">Die-Methode gibt keinen Zeiger mehr auf ein Array von Eigenschaftswerten zurück.</span><span class="sxs-lookup"><span data-stu-id="d45ff-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d45ff-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d45ff-122">See also</span></span>



[<span data-ttu-id="d45ff-123">Erste Schritte mit der Outlook-MAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d45ff-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

