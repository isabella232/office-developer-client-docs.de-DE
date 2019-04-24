---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327587"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="ff70c-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="ff70c-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="ff70c-104">Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar.</span><span class="sxs-lookup"><span data-stu-id="ff70c-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ff70c-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ff70c-105">Quick info</span></span>

<span data-ttu-id="ff70c-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ff70c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff70c-107">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ff70c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ff70c-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="ff70c-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="ff70c-109">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="ff70c-109">Property type:</span></span>  <br/> |<span data-ttu-id="ff70c-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff70c-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff70c-111">Property-Tag:</span><span class="sxs-lookup"><span data-stu-id="ff70c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ff70c-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="ff70c-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="ff70c-113">Access</span><span class="sxs-lookup"><span data-stu-id="ff70c-113">Access:</span></span>  <br/> |<span data-ttu-id="ff70c-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff70c-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff70c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff70c-115">Remarks</span></span>

<span data-ttu-id="ff70c-116">Rufen Sie diese Eigenschaft mithilfe von [IOlkAccount:: getprop](iolkaccount-getprop.md)ab.</span><span class="sxs-lookup"><span data-stu-id="ff70c-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="ff70c-117">Der Standardordner für gesendete Elemente ist " **Gesendete Elemente**".</span><span class="sxs-lookup"><span data-stu-id="ff70c-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="ff70c-118">Diese Eigenschaft ist für POP3-und IMAP-Konten schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ff70c-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="ff70c-119">Bei dem Versuch, diese Eigenschaft für diese Kontentypen festzulegen, wird **E_ACCT_NOT_FOUND**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff70c-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

