---
title: QueryDef.DateCreated-Eigenschaft (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3eb3d4664f6fce30812904612f458d24f3a8b159
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927025"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="c6dd4-102">QueryDef.DateCreated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c6dd4-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="c6dd4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6dd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6dd4-p101">Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6dd4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6dd4-106">Syntax</span></span>

<span data-ttu-id="c6dd4-107">*Ausdruck* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="c6dd4-107">*expression* .DateCreated</span></span>

<span data-ttu-id="c6dd4-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6dd4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6dd4-109">Remarks</span></span>

<span data-ttu-id="c6dd4-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

