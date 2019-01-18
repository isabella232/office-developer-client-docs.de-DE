---
title: Festlegen des Formats für DCOM-Datenstrommarshalling
TOCTitle: Setting DCOM stream marshaling format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09463552faff9c4b74b73379385ab8ba55b4f62c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698043"
---
# <a name="setting-dcom-stream-marshaling-format"></a>Festlegen des Formats für DCOM-Datenstrommarshalling


**Betrifft**: Access 2013, Office 2013

Ein Clientcomputer, auf dem Komponenten von RDS 1.5 oder früher verwendet werden, ist nicht mit einem Server kompatibel, auf dem Komponenten von RDS 2.0 oder höher verwendet werden. Wenn DCOM als zugrunde liegendes Protokoll verwendet wird, ist die Unterstützung für RDS 2.0 oder höher effizienter beim Transportieren von [Recordset](recordset-object-ado.md)-Objekten. Wenn auf dem Client Komponenten von RDS 1.5 oder früher ausgeführt werden, können Sie für den Server festlegen, dass er mit der früheren RDS-Unterstützung (RDS 1.0) oder der neueren RDS-Unterstützung (RDS 2.0 oder höher) funktionsfähig ist. Legen Sie einen der folgenden Registrierungseinträge fest:

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-oder -

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

