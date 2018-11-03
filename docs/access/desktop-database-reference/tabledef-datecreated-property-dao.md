---
title: TableDef.DateCreated-Eigenschaft (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be76ed7f9d358963ea58776327ddafbb66f9d367
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923140"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="dbf08-102">TableDef.DateCreated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="dbf08-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="dbf08-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbf08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dbf08-p101">Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="dbf08-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf08-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf08-106">Syntax</span></span>

<span data-ttu-id="dbf08-107">*Ausdruck* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="dbf08-107">*expression* .DateCreated</span></span>

<span data-ttu-id="dbf08-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="dbf08-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf08-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbf08-109">Remarks</span></span>

<span data-ttu-id="dbf08-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="dbf08-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

