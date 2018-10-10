---
title: URL-Eigenschaft (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8d1e524df8f1921f712f9dce174ab90ebd57325
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472621"
---
# <a name="url-property-rds"></a><span data-ttu-id="095c9-102">URL-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="095c9-102">URL Property (RDS)</span></span>


<span data-ttu-id="095c9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="095c9-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="095c9-104">Gibt eine Zeichenfolge an, die eine relative oder absolute URL enthält.</span><span class="sxs-lookup"><span data-stu-id="095c9-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="095c9-105">Sie können die **URL** -Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [DataControl](datacontrol-object-rds.md)-Objekts oder zur Laufzeit in Skriptcode festlegen.</span><span class="sxs-lookup"><span data-stu-id="095c9-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="095c9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="095c9-106">Syntax</span></span>

<span data-ttu-id="095c9-107">Entwurfszeit: \<PARAM NAME = Wert "URL" = "Server"\></span><span class="sxs-lookup"><span data-stu-id="095c9-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="095c9-108">Laufzeit: DataControl.URL="Server"</span><span class="sxs-lookup"><span data-stu-id="095c9-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="095c9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="095c9-109">Parameters</span></span>

  - <span data-ttu-id="095c9-110">*Server*</span><span class="sxs-lookup"><span data-stu-id="095c9-110">*Server*</span></span>

  - <span data-ttu-id="095c9-111">Ein **String** -Wert, der eine gültige URL enthält.</span><span class="sxs-lookup"><span data-stu-id="095c9-111">A **String** value that contains a valid URL.</span></span>

  - <span data-ttu-id="095c9-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="095c9-112">*DataControl*</span></span>

  - <span data-ttu-id="095c9-113">Eine Objektvariable, die ein **DataControl** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="095c9-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="095c9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="095c9-114">Remarks</span></span>

<span data-ttu-id="095c9-p101">In der Regel identifiziert die URL eine ASP-Datei (Active Server Page), die ein [Recordset](recordset-object-ado.md)-Objekt erstellen und zurückgeben kann. Dadurch erhält der Benutzer ein **Recordset** -Objekt, ohne dass er das serverbasierte [DataFactory](datafactory-object-rdsserver.md)-Objekt aufrufen oder ein benutzerdefiniertes Geschäftsobjekt programmieren muss.</span><span class="sxs-lookup"><span data-stu-id="095c9-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="095c9-117">Wenn die **URL** -Eigenschaft festgelegt wurde, sendet die [SubmitChanges](submitchanges-method-rds.md)-Methode Änderungen an den Speicherort, der durch die URL angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="095c9-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

