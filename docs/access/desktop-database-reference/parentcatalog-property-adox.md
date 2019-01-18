---
title: ParentCatalog-Eigenschaft (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707458"
---
# <a name="parentcatalog-property-adox"></a>ParentCatalog-Eigenschaft (ADOX)


**Betrifft**: Access 2013, Office 2013

Gibt den übergeordneten Katalog einer Tabelle oder einer Spalte an, um Zugriff auf providerspezifische Eigenschaften bereitzustellen.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt ein [Catalog](catalog-object-adox.md)-Objekt fest bzw. gibt dieses zurück. Das Festlegen von **ParentCatalog** auf ein geöffnetes **Catalog** -Objekt ermöglicht den Zugriff auf providerspezifische Eigenschaften vor dem Anfügen einer Tabelle oder einer Spalte an eine **Catalog** -Auflistung.

## <a name="remarks"></a>Hinweise

Einige Datenanbieter lassen das Schreiben von anbieterspezifischen Werten nur zum Erstellungszeitpunkt (beim Anfügen einer Tabelle oder einer Spalte an die **Catalog** -Auflistung) zu. Geben Sie das **Catalog** -Objekt zuerst in der **ParentCatalog** -Eigenschaft an, um auf diese Eigenschaften vor dem Anfügen der Objekte an ein **Catalog** -Objekt zuzugreifen.

Wenn die Tabelle oder die Spalte an ein anderes **Catalog** -Objekt angefügt wird, als unter **ParentCatalog** angegeben wurde, tritt ein Fehler auf.

