---
title: Erforderliche Anbieter für die Datenstrukturierung
TOCTitle: Required Providers for Data Shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de8634503c81bd2c66eeda0c64a8b1ff1b6f5363
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885353"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="6db79-102">Erforderliche Anbieter für die Datenstrukturierung</span><span class="sxs-lookup"><span data-stu-id="6db79-102">Required Providers for Data Shaping</span></span>


<span data-ttu-id="6db79-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6db79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6db79-p101">Für die Datenstrukturierung sind normalerweise zwei Anbieter erforderlich. Vom Dienstanbieter ([Datenstrukturierungsdienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)) wird die Datenstrukturierungsfunktionalität bereitgestellt, und von einem Datenanbieter, wie z. B. dem OLE DB-Anbieter für SQL Server, werden Zeilen mit Daten zum Auffüllen des geformten [Recordset](recordset-object-ado.md)-Objekts bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6db79-p101">Data shaping typically requires two providers. The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="6db79-106">Der Name des Dienstanbieters (MSDataShape) kann als Wert der [Provider](connection-object-ado.md)-Eigenschaft des [Connection](provider-property-ado.md)-Objekts oder des Verbindungszeichenfolgen-Schlüsselworts "Provider=MSDataShape;" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6db79-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="6db79-107">Der Name des Datenanbieters angegeben werden kann, als der Wert der dynamischen **Datenanbieter** -Eigenschaft, die der [Properties](properties-collection-ado.md) -Auflistung des **Connection** -Objekts vom Data Shaping Dienst für OLE DB oder des Verbindungszeichenfolgen-Schlüsselworts hinzugefügt wird "\* *Data Provider = \*\*\* Anbieter*".</span><span class="sxs-lookup"><span data-stu-id="6db79-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="6db79-p102">Wenn das **Recordset**-Objekt nicht aufgefüllt wird (z. B. bei einem erstellten **Recordset**-Objekt, in dem Spalten mit dem NEW-Schlüsselwort erstellt werden), ist kein Datenprovider erforderlich. Geben Sie in diesem Fall **"Data Provider=none;"** an.</span><span class="sxs-lookup"><span data-stu-id="6db79-p102">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword). In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="6db79-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6db79-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

