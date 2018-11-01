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
# <a name="setting-dcom-stream-marshaling-format"></a>Festlegen des DCOM-Formats für Datenstrommarshalling


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

