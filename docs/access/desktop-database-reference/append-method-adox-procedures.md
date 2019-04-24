---
title: Append-Methode (ADOX Procedures)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297081"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="7e74d-102">Append-Methode (ADOX Procedures)</span><span class="sxs-lookup"><span data-stu-id="7e74d-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="7e74d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e74d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e74d-104">Fügt der [Procedures](procedures-collection-adox.md)-Auflistung ein neues [Procedure](procedure-object-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e74d-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e74d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e74d-105">Syntax</span></span>

<span data-ttu-id="7e74d-106">*Verfahren*. Append*Name*, *Command*</span><span class="sxs-lookup"><span data-stu-id="7e74d-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="7e74d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e74d-107">Parameters</span></span>

|<span data-ttu-id="7e74d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e74d-108">Parameter</span></span>|<span data-ttu-id="7e74d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e74d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7e74d-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="7e74d-110">*Name*</span></span> |<span data-ttu-id="7e74d-111">Ein **String** -Wert, der den Namen der zu erstellenden und anzufügenden Prozedur angibt.</span><span class="sxs-lookup"><span data-stu-id="7e74d-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="7e74d-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="7e74d-112">*Command*</span></span> |<span data-ttu-id="7e74d-113">Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende und anzufügende Prozedur darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e74d-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7e74d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e74d-114">Remarks</span></span>

<span data-ttu-id="7e74d-115">Erstellt eine neue Prozedur in der Datenquelle mit dem Namen und den Attributen, die im **Command**-Objekt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7e74d-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="7e74d-p101">Wenn der vom Benutzer angegebene Befehlstext eine Sicht statt einer Prozedur darstellt, ist das Verhalten vom jeweils verwendeten Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7e74d-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="7e74d-p102">Bei Verwendung des OLE DB-Anbieters für Microsoft Jet und der **Append**-Methode der **Procedures**-Auflistung können Sie im *Command*-Parameter ein **View**-Objekt statt eines **Procedure**-Objekts angeben. Das **View**-Objekt wird der Datenquelle und der **Procedures**-Auflistung hinzugefügt. Wenn die **Procedures**- und die **Views**-Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **View**-Objekt nicht mehr in der **Procedures**-Auflistung, sondern in der **Views**-Auflistung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e74d-p102">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter. The **View** will be added to the data source and will be added to the **Procedures** collection. After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


