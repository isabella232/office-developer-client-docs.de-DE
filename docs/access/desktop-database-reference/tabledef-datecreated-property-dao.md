---
title: TableDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ffad5b1bee5756c969f03a920f453f1d3abf9e3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473311"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="3b490-102">TableDef.DateCreated Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b490-102">TableDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="3b490-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b490-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3b490-p101">Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="3b490-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b490-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b490-106">Syntax</span></span>

<span data-ttu-id="3b490-107">*Ausdruck* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="3b490-107">*expression* .DateCreated</span></span>

<span data-ttu-id="3b490-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b490-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b490-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b490-109">Remarks</span></span>

<span data-ttu-id="3b490-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3b490-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

