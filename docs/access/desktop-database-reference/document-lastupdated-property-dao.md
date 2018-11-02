---
title: Document.LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57fb558330c602206831c1c72f09a13094eba799
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927312"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="a4bec-102">Document.LastUpdated-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="a4bec-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="a4bec-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4bec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4bec-p101">Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.</span><span class="sxs-lookup"><span data-stu-id="a4bec-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4bec-106">Syntax</span></span>

<span data-ttu-id="a4bec-107">*Ausdruck* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="a4bec-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="a4bec-108">*Ausdruck* Eine Variable, die ein **Document** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4bec-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4bec-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4bec-109">Remarks</span></span>

<span data-ttu-id="a4bec-p102">DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a4bec-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

