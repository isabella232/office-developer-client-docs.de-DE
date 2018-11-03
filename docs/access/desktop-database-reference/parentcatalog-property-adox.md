---
title: ParentCatalog-Eigenschaft (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bbeed0283eaf7982d037cfe7bf4773db9a8c03b5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928453"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="18a65-102">ParentCatalog-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="18a65-102">ParentCatalog property (ADOX)</span></span>


<span data-ttu-id="18a65-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18a65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18a65-104">Gibt den übergeordneten Katalog einer Tabelle oder einer Spalte an, um Zugriff auf providerspezifische Eigenschaften bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="18a65-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="18a65-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="18a65-105">Settings and return values</span></span>

<span data-ttu-id="18a65-p101">Legt ein [Catalog](catalog-object-adox.md)-Objekt fest bzw. gibt dieses zurück. Das Festlegen von **ParentCatalog** auf ein geöffnetes **Catalog** -Objekt ermöglicht den Zugriff auf providerspezifische Eigenschaften vor dem Anfügen einer Tabelle oder einer Spalte an eine **Catalog** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="18a65-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="18a65-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18a65-108">Remarks</span></span>

<span data-ttu-id="18a65-p102">Einige Datenanbieter lassen das Schreiben von anbieterspezifischen Werten nur zum Erstellungszeitpunkt (beim Anfügen einer Tabelle oder einer Spalte an die **Catalog** -Auflistung) zu. Geben Sie das **Catalog** -Objekt zuerst in der **ParentCatalog** -Eigenschaft an, um auf diese Eigenschaften vor dem Anfügen der Objekte an ein **Catalog** -Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="18a65-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="18a65-111">Wenn die Tabelle oder die Spalte an ein anderes **Catalog** -Objekt angefügt wird, als unter **ParentCatalog** angegeben wurde, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="18a65-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>

