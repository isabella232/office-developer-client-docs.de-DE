---
title: Festlegen des Formats für Datenstrommarshalling DCOM
TOCTitle: Setting DCOM stream marshaling format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88fc34937910ba2439c796a2cec5afa8db43a0a3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944165"
---
# <a name="setting-dcom-stream-marshaling-format"></a><span data-ttu-id="6eadb-102">Festlegen des Formats für Datenstrommarshalling DCOM</span><span class="sxs-lookup"><span data-stu-id="6eadb-102">Setting DCOM stream marshaling format</span></span>


<span data-ttu-id="6eadb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6eadb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6eadb-p101">Ein Clientcomputer, auf dem Komponenten von RDS 1.5 oder früher verwendet werden, ist nicht mit einem Server kompatibel, auf dem Komponenten von RDS 2.0 oder höher verwendet werden. Wenn DCOM als zugrunde liegendes Protokoll verwendet wird, ist die Unterstützung für RDS 2.0 oder höher effizienter beim Transportieren von [Recordset](recordset-object-ado.md)-Objekten. Wenn auf dem Client Komponenten von RDS 1.5 oder früher ausgeführt werden, können Sie für den Server festlegen, dass er mit der früheren RDS-Unterstützung (RDS 1.0) oder der neueren RDS-Unterstützung (RDS 2.0 oder höher) funktionsfähig ist. Legen Sie einen der folgenden Registrierungseinträge fest:</span><span class="sxs-lookup"><span data-stu-id="6eadb-p101">A client computer using components from RDS 1.5 or earlier is not compatible with a server using components from RDS 2.0 or later. When using DCOM as the underlying protocol, the support for RDS 2.0 or later is more efficient in transporting [Recordset](recordset-object-ado.md) objects. If your client is running components from RDS 1.5 or earlier, you can set your server to work with the previous RDS support (called RDS 1.0) or the newer RDS support (called RDS 2.0 or later). Set either of the following registry entries:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

<span data-ttu-id="6eadb-108">\-oder -</span><span class="sxs-lookup"><span data-stu-id="6eadb-108">\-or-</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

