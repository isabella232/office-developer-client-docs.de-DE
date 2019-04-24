---
title: Supports-Methode (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308463"
---
# <a name="supports-method-ado"></a><span data-ttu-id="dd654-102">Supports-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd654-102">Supports method (ADO)</span></span>

<span data-ttu-id="dd654-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd654-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd654-104">Bestimmt, ob ein angegebenes [Recordset](recordset-object-ado.md)-Objekt einen bestimmten Funktionalitätstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd654-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd654-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd654-105">Syntax</span></span>

<span data-ttu-id="dd654-106">*Boolesches* = *Recordset*-Objekt. Unterstützt (*Cursor*Options)</span><span class="sxs-lookup"><span data-stu-id="dd654-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="dd654-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd654-107">Return value</span></span>

<span data-ttu-id="dd654-108">Gibt einen **Boolean**-Wert zurück, der kennzeichnet, ob alle vom *CursorOptions*-Argument identifizierten Features vom Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dd654-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd654-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd654-109">Parameters</span></span>

|<span data-ttu-id="dd654-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd654-110">Parameter</span></span>|<span data-ttu-id="dd654-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd654-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dd654-112">*Cursor Options*</span><span class="sxs-lookup"><span data-stu-id="dd654-112">*CursorOptions*</span></span> |<span data-ttu-id="dd654-113">Ein Ausdruck vom Datentyp **Long**, der aus mindestens einem [CursorOptionEnum](cursoroptionenum.md)-Wert besteht.</span><span class="sxs-lookup"><span data-stu-id="dd654-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dd654-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd654-114">Remarks</span></span>

<span data-ttu-id="dd654-p101">Mit der **Supports**-Methode bestimmen Sie, welche Funktionalität ein **Recordset**-Objekt unterstützt. Wenn das **Recordset**-Objekt die Features unterstützt, deren entsprechende Konstanten in *CursorOptions* enthalten sind, gibt die **Supports**-Methode **True** zurück. Andernfalls wird **False** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd654-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="dd654-p102">[!HINWEIS] Die **Supports** -Methode kann zwar **True** für eine bestimmte Funktionalität zurückgeben, aber dies garantiert nicht, dass der Anbieter das Feature unter allen Umständen zur Verfügung stellen kann. Die **Supports** -Methode gibt einfach zurück, ob der Anbieter die angegebene Funktionalität unterstützen kann, vorausgesetzt bestimmte Bedingungen sind erfüllt. Beispielsweise kann die **Supports** -Methode angeben, dass ein **Recordset** -Objekt Aktualisierungen unterstützt, obwohl der Cursor auf einer Verknüpfung mehrerer Tabellen basiert, von denen manche Spalten nicht aktualisierbar sind.</span><span class="sxs-lookup"><span data-stu-id="dd654-p102">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>


