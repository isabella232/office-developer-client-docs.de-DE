---
title: Implementieren der IUnknown-Schnittstelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310045"
---
# <a name="implementing-the-iunknown-interface"></a>Implementieren der IUnknown-Schnittstelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Methoden der [IUnknown-Schnittstelle,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) die in jedem MAPI-Objekt implementiert sind, unterstützen die Kommunikation zwischen Objekten und die Objektverwaltung. 
  
 **IUnknown** hat drei Methoden: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)und [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **Mit QueryInterface** kann ein Objekt bestimmen, ob ein anderes Objekt eine bestimmte Schnittstelle unterstützt. Mit **QueryInterface** können zwei Objekte interagieren, die sich nicht über die Funktionalität der anderen benutzerintern im Voraus kennen. Wenn das Objekt, das **QueryInterface** implementiert, die in Frage gestellte Schnittstelle unterstützt, gibt es einen Zeiger auf die Implementierung der Schnittstelle zurück. Wenn das Objekt die angeforderte Schnittstelle nicht unterstützt, gibt es den wert MAPI_E_INTERFACE_NOT_SUPPORTED zurück. 
  
Wenn **QueryInterface** einen angeforderten Schnittstellenzeiger zurückgibt, muss auch die Referenzanzahl des neuen Objekts erhöht werden. Die Referenzanzahl eines Objekts ist ein numerischer Wert, der zum Verwalten der Lebensdauer des Objekts verwendet wird. Wenn die Referenzanzahl größer als 1 ist, kann der Arbeitsspeicher des Objekts nicht frei werden, da es aktiv verwendet wird. Nur wenn die Referenzanzahl auf 0 fällt, kann das Objekt sicher freigegeben werden. 
  
Die beiden anderen **IUnknown-Methoden** **AddRef** und **Release** verwalten die Referenzanzahl. **AddRef** erhöht die Referenzanzahl, während **Release** sie dekrementiert. Alle Methoden oder API-Funktionen, die Schnittstellenzeiger zurückgeben, z. B. **QueryInterface**, müssen **AddRef aufrufen,** um die Referenzanzahl zu erhöhen. Alle Implementierungen von Methoden, die Schnittstellenzeiger empfangen, müssen **Release** aufrufen, um die Anzahl zu dekrementieren, wenn der Zeiger nicht mehr benötigt wird. **Die** Freigabe überprüft auf eine vorhandene Referenzanzahl und gibt den der Schnittstelle zugeordneten Arbeitsspeicher nur frei, wenn die Anzahl 0 ist. 
  
> [!NOTE]
> Da **AddRef** und **Release** keine genauen Werte zurückgeben müssen, dürfen Aufrufer dieser Methoden die Rückgabewerte nicht verwenden, um zu ermitteln, ob ein Objekt noch gültig ist oder zerstört wurde. 
  
## <a name="see-also"></a>Siehe auch



[Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

