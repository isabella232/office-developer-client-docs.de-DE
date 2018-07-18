---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto an.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791182"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="f5708-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="f5708-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="f5708-104">Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="f5708-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f5708-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f5708-105">Quick info</span></span>

<span data-ttu-id="f5708-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="f5708-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5708-107">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f5708-107">Identifier:</span></span>  <br/> |<span data-ttu-id="f5708-108">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="f5708-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="f5708-109">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="f5708-109">Property type:</span></span>  <br/> |<span data-ttu-id="f5708-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f5708-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f5708-111">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="f5708-111">Property tag:</span></span>  <br/> |<span data-ttu-id="f5708-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="f5708-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="f5708-113">Access:</span><span class="sxs-lookup"><span data-stu-id="f5708-113">Access:</span></span>  <br/> |<span data-ttu-id="f5708-114">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f5708-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5708-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5708-115">Remarks</span></span>

<span data-ttu-id="f5708-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="f5708-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="f5708-117">**Gesendete Elemente**ist der Standardordner für gesendete Elemente.</span><span class="sxs-lookup"><span data-stu-id="f5708-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="f5708-118">Diese Eigenschaft ist schreibgeschützt für POP3- und IMAP-Konten.</span><span class="sxs-lookup"><span data-stu-id="f5708-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="f5708-119">Sie versuchen, diese Eigenschaft für diese Typen von Konten festzulegen, gibt **E_ACCT_NOT_FOUND**zurück.</span><span class="sxs-lookup"><span data-stu-id="f5708-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

