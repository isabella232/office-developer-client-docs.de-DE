---
title: Microsoft Data Shaping Dienst für OLE DB (ADO-Dienstanbieter)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a72dcc754f39144da4476c9262b93b920fbfbdf6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474544"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="3fe39-102">Microsoft Data Shaping Dienst für OLE DB (ADO-Dienstanbieter)</span><span class="sxs-lookup"><span data-stu-id="3fe39-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="3fe39-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fe39-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3fe39-104">Der Dienstanbieter Microsoft Data Shaping Dienst für OLE DB unterstützt das Erstellen von hierarchischen (strukturierten) [Recordset](recordset-object-ado.md)-Objekten aus einem Datenanbieter.</span><span class="sxs-lookup"><span data-stu-id="3fe39-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="3fe39-105">Schlüsselwort für den Anbieter</span><span class="sxs-lookup"><span data-stu-id="3fe39-105">Provider Keyword</span></span>

<span data-ttu-id="3fe39-106">Um den Data Shaping Service for OLE DB aufzurufen, geben Sie das folgende Schlüsselwort und den folgenden Wert in die Verbindungszeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="3fe39-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="3fe39-107">Dynamische Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3fe39-107">Dynamic Properties</span></span>

<span data-ttu-id="3fe39-108">Beim Aufrufen dieses Dienstanbieters werden der [Properties](connection-object-ado.md)-Auflistung des [Connection](properties-collection-ado.md)-Objekts die folgenden dynamischen Eigenschaften hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3fe39-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fe39-109">Name der dynamischen Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3fe39-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="3fe39-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fe39-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fe39-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="3fe39-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="3fe39-112">Gibt an, ob <strong>Recordset</strong> -Objekte mit doppelten Werten für deren Eigenschaften <strong>Reshape Name</strong> zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3fe39-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="3fe39-113">Wenn diese dynamische Eigenschaft <strong>True ist</strong> und ein neues <strong>Recordset-Objekt</strong> wird erstellt, mit derselben vom Benutzer angegebener reshape Name als ein bereits vorhandenes <strong>Recordset-Objekt</strong>, und klicken Sie dann das neue <strong>Recordset</strong> -Objekt Reshape Name wird geändert, damit es eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="3fe39-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="3fe39-114">Wenn diese Eigenschaft <strong>False</strong> ist, und ein neues <strong>Recordset-Objekt</strong> wird erstellt, mit derselben vom Benutzer angegebener reshape Name als den vorhandenen <strong>Recordset</strong>, beide <strong>Recordset</strong> -Objekte haben dieselbe reshape Name.</span><span class="sxs-lookup"><span data-stu-id="3fe39-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="3fe39-115">Aus diesem Grund kann weder <strong>Recordset</strong> strukturiert werden, solange beide Objekte vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3fe39-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="3fe39-116">Der Standardwert der Eigenschaft lautet <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="3fe39-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fe39-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="3fe39-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="3fe39-p102">Gibt den Namen des Anbieters an, der Zeilen zum Strukturieren bereitstellt. Dieser Wert kann NONE sein, wenn der Anbieter nicht zum Bereitstellen von Zeilen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3fe39-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fe39-p103">Sie können auch beschreibbare dynamische Eigenschaften festlegen, indem Sie die zugehörigen Namen in der Verbindungszeichenfolge als Schlüsselwörter angeben. Legen Sie beispielsweise in Microsoft Visual Basic die dynamische Eigenschaft Data Provider auf MSDASQL fest, indem Sie Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="3fe39-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="3fe39-p104">Sie können auch eine dynamische Eigenschaft festlegen oder abrufen, indem Sie deren Namen als Index für die [Properties](properties-collection-ado.md)-Eigenschaft angeben. Beispiel: Rufen Sie den aktuellen Wert der dynamischen Eigenschaft **Data Provider** ab, und drucken Sie ihn. Legen Sie anschließend einen neuen Wert fest. Gehen Sie dazu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="3fe39-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="3fe39-124">Weitere Informationen zur Datenstrukturierung finden Sie unter [Datenstrukturierung (Zusammenfassung)](data-shaping-summary.md).</span><span class="sxs-lookup"><span data-stu-id="3fe39-124">For more information about data shaping, see [Data Shaping](data-shaping-summary.md).</span></span>

