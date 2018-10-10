---
title: Supports-Methode (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61e6a4f3a5771c4d223380160204e4b0b350f210
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472670"
---
# <a name="supports-method-ado"></a><span data-ttu-id="b932d-102">Supports-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="b932d-102">Supports Method (ADO)</span></span>


<span data-ttu-id="b932d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b932d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b932d-104">Bestimmt, ob ein angegebenes [Recordset](recordset-object-ado.md)-Objekt einen bestimmten Funktionalitätstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b932d-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="b932d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b932d-105">Syntax</span></span>

<span data-ttu-id="b932d-106">*Boolean* = *Recordset-Objekt*. Unterstützt (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="b932d-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="b932d-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b932d-107">Return Value</span></span>

<span data-ttu-id="b932d-108">Gibt einen **booleschen** Wert, der angibt, ob alle vom *CursorOptions* -Argument identifizierten Features vom Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b932d-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="b932d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b932d-109">Parameters</span></span>

  - <span data-ttu-id="b932d-110">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="b932d-110">*CursorOptions*</span></span>

  - <span data-ttu-id="b932d-111">Ein Ausdruck vom Datentyp **Long**, der aus mindestens einem [CursorOptionEnum](cursoroptionenum.md)-Wert besteht.</span><span class="sxs-lookup"><span data-stu-id="b932d-111">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b932d-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b932d-112">Remarks</span></span>

<span data-ttu-id="b932d-p101">Mit der **Supports**-Methode bestimmen Sie, welche Funktionalität ein **Recordset**-Objekt unterstützt. Wenn das **Recordset**-Objekt die Features unterstützt, deren entsprechende Konstanten in *CursorOptions* enthalten sind, gibt die **Supports**-Methode **True** zurück. Andernfalls wird **False** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b932d-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b932d-p102">[!HINWEIS] Die <STRONG>Supports</STRONG> -Methode kann zwar <STRONG>True</STRONG> für eine bestimmte Funktionalität zurückgeben, aber dies garantiert nicht, dass der Anbieter das Feature unter allen Umständen zur Verfügung stellen kann. Die <STRONG>Supports</STRONG> -Methode gibt einfach zurück, ob der Anbieter die angegebene Funktionalität unterstützen kann, vorausgesetzt bestimmte Bedingungen sind erfüllt. Beispielsweise kann die <STRONG>Supports</STRONG> -Methode angeben, dass ein <STRONG>Recordset</STRONG> -Objekt Aktualisierungen unterstützt, obwohl der Cursor auf einer Verknüpfung mehrerer Tabellen basiert, von denen manche Spalten nicht aktualisierbar sind.</span><span class="sxs-lookup"><span data-stu-id="b932d-p102">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>


