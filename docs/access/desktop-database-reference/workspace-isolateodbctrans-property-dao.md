---
title: Workspace.IsolateODBCTrans-Eigenschaft (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e0649fd29a2bed21a894334b34cfe64bc9b3563
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930042"
---
# <a name="workspaceisolateodbctrans-property-dao"></a><span data-ttu-id="08b89-102">Workspace.IsolateODBCTrans-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="08b89-102">Workspace.IsolateODBCTrans property (DAO)</span></span>


<span data-ttu-id="08b89-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08b89-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08b89-104">Legt einen Wert fest, der angibt, ob mehrere Transaktionen, die dieselbe mit der Microsoft Access-Datenbank-Engine verbundene ODBC-Datenquelle verwenden, isoliert sind, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="08b89-104">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="08b89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08b89-105">Syntax</span></span>

<span data-ttu-id="08b89-106">*Ausdruck* . IsolateODBCTrans</span><span class="sxs-lookup"><span data-stu-id="08b89-106">*expression* .IsolateODBCTrans</span></span>

<span data-ttu-id="08b89-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="08b89-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="08b89-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08b89-108">Remarks</span></span>

<span data-ttu-id="08b89-p101">Es gibt Situationen, in denen mehrere gleichzeitige Transaktionen für dieselbe ODBC-Verbindung zur Verarbeitung anstehen müssen. Hierzu müssen Sie für jede Transaktion ein eigenes **Workspace**-Objekt öffnen. Wenngleich jedes **Workspace**-Objekt seine eigene ODBC-Verbindung zur Datenbank haben kann, wird dadurch die Systemleistung beeinträchtigt. Da gewöhnlich keine Transaktionsisolation erforderlich ist, können ODBC-Verbindungen von mehreren **Workspace**-Objekten, die von einem Benutzer geöffnet wurden, standardmäßig gemeinsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b89-p101">In some situations, you need to have multiple simultaneous transactions pending on the same ODBC connection. To do this, you need to open a separate **Workspace** for each transaction. Although each **Workspace** can have its own ODBC connection to the database, this slows system performance. Because transaction isolation isn't usually required, ODBC connections from multiple **Workspace** objects opened by the same user are shared by default.</span></span>

<span data-ttu-id="08b89-p102">Einige ODBC-Server, wie etwa Microsoft SQL Server, gestatten keine gleichzeitigen Transaktionen über eine einzelne Verbindung. Wenn in einer solchen Datenbank mehrere Transaktionen gleichzeitig ausstehen, legen Sie für jedes **Workspace**-Objekt sofort nach dem Öffnen den Wert der **IsolateODBCTrans**-Eigenschaft auf **True** fest. Dadurch wird für jedes **Workspace**-Objekt eine separate ODBC-Verbindung erzwungen.</span><span class="sxs-lookup"><span data-stu-id="08b89-p102">Some ODBC servers, such as Microsoft SQL Server, don't allow simultaneous transactions on a single connection. If you need to have more than one transaction at a time pending against such a database, set the **IsolateODBCTrans** property to **True** on each **Workspace** as soon as you open it. This forces a separate ODBC connection for each **Workspace**.</span></span>

