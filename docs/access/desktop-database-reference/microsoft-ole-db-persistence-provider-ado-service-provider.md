---
title: Microsoft OLE DB-Anbieter für Persistenz (ADO-Dienstanbieter)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715508"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="152c9-102">Microsoft OLE DB-Anbieter für Persistenz (ADO-Dienstanbieter)</span><span class="sxs-lookup"><span data-stu-id="152c9-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="152c9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="152c9-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="152c9-104">Microsoft OLE DB-Anbieter für Persistenz können Sie ein [Recordset](recordset-object-ado.md) -Objekt in einer Datei zu speichern und später dieses **Recordset** -Objekt aus der Datei wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="152c9-104">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file.</span></span> <span data-ttu-id="152c9-105">Schemainformationen, Daten und ausstehende Änderungen werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="152c9-105">Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="152c9-106">Sie können das **Recordset** -Objekt entweder im proprietären ADTG-Format (Advanced Data Table Gram) oder im offenen XML-Format (Extensible Markup Language) speichern.</span><span class="sxs-lookup"><span data-stu-id="152c9-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="152c9-107">Schlüsselwort für den Anbieter</span><span class="sxs-lookup"><span data-stu-id="152c9-107">Provider Keyword</span></span>

<span data-ttu-id="152c9-108">Um diesen Anbieter aufzurufen, geben Sie das folgende Schlüsselwort und den folgenden Wert in die Verbindungszeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="152c9-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="152c9-109">Fehler</span><span class="sxs-lookup"><span data-stu-id="152c9-109">Errors</span></span>

<span data-ttu-id="152c9-110">Die folgenden Fehler, die von diesem Anbieter ausgegeben werden, können in Ihrer Anwendung erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="152c9-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="152c9-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="152c9-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="152c9-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="152c9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="152c9-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="152c9-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="152c9-114">Die geöffnete Datei weist kein gültiges Format auf (d. h. das Format ist weder ADTG noch XML).</span><span class="sxs-lookup"><span data-stu-id="152c9-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="152c9-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="152c9-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="152c9-116">Das <strong>Recordset</strong>-Objekt weist Merkmale auf, die verhindern, dass das Objekt gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="152c9-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="152c9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="152c9-117">Remarks</span></span>

<span data-ttu-id="152c9-118">Der Microsoft OLE DB-Anbieter für Persistenz macht keine dynamischen Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="152c9-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="152c9-119">Derzeit können nur parametrisierte hierarchische **Recordset** -Objekte nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="152c9-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="152c9-120">Weitere Informationen zum permanenten Speichern von **Recordset** -Objekten finden Sie unter [Weitere Informationen zur Permanenz von Recordsets ](more-about-recordset-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="152c9-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="152c9-121">Beim Öffnen eines **Recordset-Objekts**ein Stream verwendet wird, gibt es soll keine Parameter angegeben, andere als die *Source* -Parameter der **Open** -Methode.</span><span class="sxs-lookup"><span data-stu-id="152c9-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

