---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564171"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="04cdf-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04cdf-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="04cdf-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04cdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04cdf-105">Enthält Informationen zur Unterstützung für einen Ordner für die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="04cdf-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04cdf-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="04cdf-106">Provided by:</span></span>  <br/> |<span data-ttu-id="04cdf-107">Nachricht Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="04cdf-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="04cdf-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="04cdf-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="04cdf-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="04cdf-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="04cdf-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="04cdf-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04cdf-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="04cdf-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="04cdf-112">Ruft Informationen über die Unterstützung für einen Ordner für die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="04cdf-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04cdf-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="04cdf-113">Remarks</span></span>

<span data-ttu-id="04cdf-114">Im Allgemeinen erfordert Microsoft Office Outlook MAPI-Speicheranbieter diese Schnittstelle implementieren, wenn der Anbieter einen Ordner freigeben möchte.</span><span class="sxs-lookup"><span data-stu-id="04cdf-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="04cdf-115">Die Ausnahme ist der Exchange-Server-Speicher-Anbieter, der Ordner freigeben kann, ohne dass diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="04cdf-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="04cdf-116">Ein Client kann ein **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**Abfragen.</span><span class="sxs-lookup"><span data-stu-id="04cdf-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="04cdf-117">Wenn dies erfolgreich ist, rufen Sie **IFolderSupport::GetSupportMask** , und prüfen Sie, ob das Bit **FS_SUPPORTS_SHARING** festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04cdf-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

