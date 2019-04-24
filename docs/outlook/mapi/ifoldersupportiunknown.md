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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351387"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="8a194-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a194-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="8a194-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a194-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a194-105">Enthält Informationen zur Unterstützung eines Ordners für die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="8a194-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a194-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="8a194-106">Provided by:</span></span>  <br/> |<span data-ttu-id="8a194-107">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="8a194-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="8a194-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8a194-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8a194-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="8a194-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8a194-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8a194-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a194-111">**[Getsupportmask aufrufen](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="8a194-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="8a194-112">Ruft Informationen über die Unterstützung eines Ordners für die Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="8a194-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a194-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a194-113">Remarks</span></span>

<span data-ttu-id="8a194-114">Im Allgemeinen erfordert Microsoft Office Outlook einen MAPI-Speicheranbieter zum Implementieren dieser Schnittstelle, wenn der Anbieter einen Ordner freigeben möchte.</span><span class="sxs-lookup"><span data-stu-id="8a194-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="8a194-115">Die Ausnahme ist der Exchange Server-Speicheranbieter, der Ordner freigeben kann, ohne diese Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="8a194-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="8a194-116">Ein Client kann eine **[IMAPIFolder](imapifolderimapicontainer.md)** für **IFolderSupport**Abfragen.</span><span class="sxs-lookup"><span data-stu-id="8a194-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="8a194-117">Wenn dies erfolgreich ist, rufen Sie **IFolderSupport:: getsupportmask aufrufen** auf, und überprüfen Sie, ob das **FS_SUPPORTS_SHARING** -Bit festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a194-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

