---
title: Supports-Methode (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceeab22cda05738fdcec090acb5b4a2d6fc88a5b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604260"
---
# <a name="supports-method-ado"></a><span data-ttu-id="17690-102">Supports-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="17690-102">Supports Method (ADO)</span></span>


<span data-ttu-id="17690-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17690-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17690-104">Bestimmt, ob ein angegebenes [Recordset](recordset-object-ado.md)-Objekt einen bestimmten Funktionalitätstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17690-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="17690-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17690-105">Syntax</span></span>

<span data-ttu-id="17690-106">*Boolean* = *Recordset-Objekt*. Unterstützt (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="17690-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

<span data-ttu-id="17690-107"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="17690-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="17690-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17690-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="17690-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17690-109">Return value</span></span>
>>>>>>> <span data-ttu-id="17690-110">master</span><span class="sxs-lookup"><span data-stu-id="17690-110">master</span></span>

<span data-ttu-id="17690-111">Gibt einen **booleschen** Wert, der angibt, ob alle vom *CursorOptions* -Argument identifizierten Features vom Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="17690-111">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="17690-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="17690-112">Parameters</span></span>

  - <span data-ttu-id="17690-113">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="17690-113">*CursorOptions*</span></span>

  - <span data-ttu-id="17690-114">Ein Ausdruck vom Datentyp **Long**, der aus mindestens einem [CursorOptionEnum](cursoroptionenum.md)-Wert besteht.</span><span class="sxs-lookup"><span data-stu-id="17690-114">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="17690-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17690-115">Remarks</span></span>

<span data-ttu-id="17690-p101">Mit der **Supports**-Methode bestimmen Sie, welche Funktionalität ein **Recordset**-Objekt unterstützt. Wenn das **Recordset**-Objekt die Features unterstützt, deren entsprechende Konstanten in *CursorOptions* enthalten sind, gibt die **Supports**-Methode **True** zurück. Andernfalls wird **False** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17690-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="17690-p102">[!HINWEIS] Die <STRONG>Supports</STRONG> -Methode kann zwar <STRONG>True</STRONG> für eine bestimmte Funktionalität zurückgeben, aber dies garantiert nicht, dass der Anbieter das Feature unter allen Umständen zur Verfügung stellen kann. Die <STRONG>Supports</STRONG> -Methode gibt einfach zurück, ob der Anbieter die angegebene Funktionalität unterstützen kann, vorausgesetzt bestimmte Bedingungen sind erfüllt. Beispielsweise kann die <STRONG>Supports</STRONG> -Methode angeben, dass ein <STRONG>Recordset</STRONG> -Objekt Aktualisierungen unterstützt, obwohl der Cursor auf einer Verknüpfung mehrerer Tabellen basiert, von denen manche Spalten nicht aktualisierbar sind.</span><span class="sxs-lookup"><span data-stu-id="17690-p102">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>


