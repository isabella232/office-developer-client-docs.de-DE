---
title: TableDef.LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81d8dfd040ef7df954b71f724ed1d2689d5d4b33
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928222"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="0dc68-102">TableDef.LastUpdated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="0dc68-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="0dc68-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dc68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0dc68-p101">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="0dc68-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc68-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dc68-106">Syntax</span></span>

<span data-ttu-id="0dc68-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="0dc68-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="0dc68-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0dc68-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc68-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0dc68-109">Remarks</span></span>

<span data-ttu-id="0dc68-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0dc68-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

