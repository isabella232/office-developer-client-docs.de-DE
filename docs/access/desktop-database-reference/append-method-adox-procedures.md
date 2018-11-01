---
title: Append-Methode (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef11c9d45cc5b34b5ef7b1cf762dfd6f3e4c1d64
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873047"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="715ae-102">Append-Methode (ADOX Procedures)</span><span class="sxs-lookup"><span data-stu-id="715ae-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="715ae-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="715ae-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="715ae-104">Fügt der [Procedures](procedure-object-adox.md)-Auflistung ein neues [Procedure](procedures-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="715ae-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="715ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="715ae-105">Syntax</span></span>

<span data-ttu-id="715ae-106">*Verfahren*. Fügen Sie*Namen*, *Befehl*</span><span class="sxs-lookup"><span data-stu-id="715ae-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="715ae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="715ae-107">Parameters</span></span>

  - <span data-ttu-id="715ae-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="715ae-108">*Name*</span></span>

  - <span data-ttu-id="715ae-109">Ein **String** -Wert, der den Namen der zu erstellenden und anzufügenden Prozedur angibt.</span><span class="sxs-lookup"><span data-stu-id="715ae-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="715ae-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="715ae-110">*Command*</span></span>

  - <span data-ttu-id="715ae-111">Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende und anzufügende Prozedur darstellt.</span><span class="sxs-lookup"><span data-stu-id="715ae-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="715ae-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="715ae-112">Remarks</span></span>

<span data-ttu-id="715ae-113">Erstellt eine neue Prozedur in der Datenquelle mit dem Namen und den Attributen, die im **Command** -Objekt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="715ae-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="715ae-p101">Wenn der vom Benutzer angegebene Befehlstext eine Sicht statt einer Prozedur darstellt, ist das Verhalten vom jeweils verwendeten Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="715ae-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="715ae-116">Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die **Append** -Methode der **Procedures** -Auflistung angeben einer **Ansicht** , sondern eine **Prozedur** in *der Befehlsparameter* ansetzt.</span><span class="sxs-lookup"><span data-stu-id="715ae-116">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="715ae-117">Das **View** -Objekt wird der Datenquelle und der **Procedures** -Auflistung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="715ae-117">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="715ae-118">Wenn die **Procedures** - und die **Views** -Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **View** -Objekt nicht mehr in der **Procedures** -Auflistung, sondern in der **Views** -Auflistung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="715ae-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


