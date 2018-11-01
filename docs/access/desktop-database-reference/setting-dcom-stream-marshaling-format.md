---
title: Festlegen des DCOM-Formats für Datenstrommarshalling
TOCTitle: Setting DCOM Stream Marshaling Format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51449286d2ddd9340f1adc883cdaff7e76429f88
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874111"
---
# <a name="setting-dcom-stream-marshaling-format"></a><span data-ttu-id="e304a-102">Festlegen des DCOM-Formats für Datenstrommarshalling</span><span class="sxs-lookup"><span data-stu-id="e304a-102">Setting DCOM Stream Marshaling Format</span></span>


<span data-ttu-id="e304a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e304a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e304a-p101">Ein Clientcomputer, auf dem Komponenten von RDS 1.5 oder früher verwendet werden, ist nicht mit einem Server kompatibel, auf dem Komponenten von RDS 2.0 oder höher verwendet werden. Wenn DCOM als zugrunde liegendes Protokoll verwendet wird, ist die Unterstützung für RDS 2.0 oder höher effizienter beim Transportieren von [Recordset](recordset-object-ado.md)-Objekten. Wenn auf dem Client Komponenten von RDS 1.5 oder früher ausgeführt werden, können Sie für den Server festlegen, dass er mit der früheren RDS-Unterstützung (RDS 1.0) oder der neueren RDS-Unterstützung (RDS 2.0 oder höher) funktionsfähig ist. Legen Sie einen der folgenden Registrierungseinträge fest:</span><span class="sxs-lookup"><span data-stu-id="e304a-p101">A client computer using components from RDS 1.5 or earlier is not compatible with a server using components from RDS 2.0 or later. When using DCOM as the underlying protocol, the support for RDS 2.0 or later is more efficient in transporting [Recordset](recordset-object-ado.md) objects. If your client is running components from RDS 1.5 or earlier, you can set your server to work with the previous RDS support (called RDS 1.0) or the newer RDS support (called RDS 2.0 or later). Set either of the following registry entries:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

<span data-ttu-id="e304a-108">\-oder -</span><span class="sxs-lookup"><span data-stu-id="e304a-108">\-or-</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

