---
title: Append-Methode (ADOX Views)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ccba425e74321f4ab760e9ddc4a722295290ffd1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925156"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="14b19-102">Append-Methode (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="14b19-102">Append method (ADOX Views)</span></span>


<span data-ttu-id="14b19-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14b19-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="14b19-104">Erstellt ein neues [View](view-object-adox.md)-Objekt und fügt es an die [Views](views-collection-adox.md)-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="14b19-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14b19-105">Syntax</span></span>

<span data-ttu-id="14b19-106">*Ansichten*. Fügen Sie*Namen*, *Befehl*</span><span class="sxs-lookup"><span data-stu-id="14b19-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="14b19-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="14b19-107">Parameters</span></span>

  - <span data-ttu-id="14b19-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="14b19-108">*Name*</span></span>

  - <span data-ttu-id="14b19-109">Ein **String** -Wert, der den Namen der zu erstellenden Sicht angibt.</span><span class="sxs-lookup"><span data-stu-id="14b19-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="14b19-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="14b19-110">*Command*</span></span>

  - <span data-ttu-id="14b19-111">Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende Sicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="14b19-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b19-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14b19-112">Remarks</span></span>

<span data-ttu-id="14b19-113">Erstellt eine neue Sicht in der Datenquelle mit dem Namen und Attributen, die im **Command** -Objekt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="14b19-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="14b19-p101">Wenn der vom Benutzer angegebene Befehlstext keine Sicht, sondern eine Prozedur darstellt, ist das Verhalten vom Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14b19-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="14b19-116">Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die **Append** -Methode der **Views** -Auflistung angeben einer **Ansicht** , sondern eine **Prozedur** in *der Befehlsparameter* ansetzt.</span><span class="sxs-lookup"><span data-stu-id="14b19-116">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="14b19-117">Das **Procedure** -Objekt wird der Datenquelle und der **Views** -Auflistung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="14b19-117">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="14b19-118">Wenn die **Procedures** - und die **Views** -Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **Procedure** -Objekt nicht mehr in der **Views** -Auflistung, sondern in der **Procedures** -Auflistung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="14b19-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


