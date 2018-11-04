---
title: Supports-Methode (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4aa04cf3d04b71e0a84279bfc5340e7ee326de48
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949627"
---
# <a name="supports-method-ado"></a><span data-ttu-id="6389a-102">Supports-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="6389a-102">Supports method (ADO)</span></span>

<span data-ttu-id="6389a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6389a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6389a-104">Bestimmt, ob ein angegebenes [Recordset](recordset-object-ado.md)-Objekt einen bestimmten Funktionalitätstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6389a-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="6389a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6389a-105">Syntax</span></span>

<span data-ttu-id="6389a-106">*Boolean* = *Recordset-Objekt*. Unterstützt (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="6389a-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="6389a-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6389a-107">Return value</span></span>

<span data-ttu-id="6389a-108">Gibt einen **booleschen** Wert, der angibt, ob alle vom *CursorOptions* -Argument identifizierten Features vom Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6389a-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="6389a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6389a-109">Parameters</span></span>

|<span data-ttu-id="6389a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6389a-110">Parameter</span></span>|<span data-ttu-id="6389a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6389a-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6389a-112">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="6389a-112">*CursorOptions*</span></span> |<span data-ttu-id="6389a-113">Ein Ausdruck vom Datentyp **Long**, der aus mindestens einem [CursorOptionEnum](cursoroptionenum.md)-Wert besteht.</span><span class="sxs-lookup"><span data-stu-id="6389a-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6389a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6389a-114">Remarks</span></span>

<span data-ttu-id="6389a-p101">Mit der **Supports**-Methode bestimmen Sie, welche Funktionalität ein **Recordset**-Objekt unterstützt. Wenn das **Recordset**-Objekt die Features unterstützt, deren entsprechende Konstanten in *CursorOptions* enthalten sind, gibt die **Supports**-Methode **True** zurück. Andernfalls wird **False** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6389a-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="6389a-p102">[!HINWEIS] Die **Supports** -Methode kann zwar **True** für eine bestimmte Funktionalität zurückgeben, aber dies garantiert nicht, dass der Anbieter das Feature unter allen Umständen zur Verfügung stellen kann. Die **Supports** -Methode gibt einfach zurück, ob der Anbieter die angegebene Funktionalität unterstützen kann, vorausgesetzt bestimmte Bedingungen sind erfüllt. Beispielsweise kann die **Supports** -Methode angeben, dass ein **Recordset** -Objekt Aktualisierungen unterstützt, obwohl der Cursor auf einer Verknüpfung mehrerer Tabellen basiert, von denen manche Spalten nicht aktualisierbar sind.</span><span class="sxs-lookup"><span data-stu-id="6389a-p102">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>


