---
title: LISTSHEETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Gibt eine Blattreferenz auf das Listencontainer-Shape zurück, das das Shape enthält.
ms.openlocfilehash: 748a248f68345e97e97ca90a4603b6e164a551c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429551"
---
# <a name="listsheetref-function"></a><span data-ttu-id="f1d80-103">LISTSHEETREF Function</span><span class="sxs-lookup"><span data-stu-id="f1d80-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="f1d80-104">Gibt eine Blattreferenz auf das Listencontainer-Shape zurück, das das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="f1d80-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="f1d80-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="f1d80-105">Version Information</span></span>

<span data-ttu-id="f1d80-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="f1d80-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f1d80-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1d80-107">Syntax</span></span>

<span data-ttu-id="f1d80-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="f1d80-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="f1d80-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1d80-109">Return value</span></span>

<span data-ttu-id="f1d80-110">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="f1d80-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1d80-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1d80-111">Remarks</span></span>

<span data-ttu-id="f1d80-112">Wenn es sich bei dem Shape nicht um ein Listenelement handelt, gibt die LISTSHEETREF-Funktion #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="f1d80-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="f1d80-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f1d80-113">Example</span></span>

<span data-ttu-id="f1d80-114">LISTSHEETREF(1)! Height</span><span class="sxs-lookup"><span data-stu-id="f1d80-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="f1d80-115">Gibt den Werte in der Zelle "Height" des Listencontainer-Shapes zurück, das das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="f1d80-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

