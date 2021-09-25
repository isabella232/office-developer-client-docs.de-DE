---
title: Implementieren der IUnknown-Schnittstelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0d307b3bda9f5e4f6c4059589f4af23698cde9f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575638"
---
# <a name="implementing-the-iunknown-interface"></a>Implementieren der IUnknown-Schnittstelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Methoden der [IUnknown-Schnittstelle,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) die in jedem MAPI-Objekt implementiert sind, unterstützen die Kommunikation zwischen Objekten und die Objektverwaltung. 
  
 **IUnknown** verfügt über drei Methoden: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)und [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **Mit QueryInterface** kann ein Objekt bestimmen, ob ein anderes Objekt eine bestimmte Schnittstelle unterstützt. Mit **QueryInterface** können zwei Objekte ohne vorherige Kenntnis der Funktionen des anderen interagieren. Wenn das Objekt, das **QueryInterface** implementiert, die betreffende Schnittstelle unterstützt, gibt es einen Zeiger auf die Implementierung der Schnittstelle zurück. Wenn das Objekt die angeforderte Schnittstelle nicht unterstützt, gibt es den MAPI_E_INTERFACE_NOT_SUPPORTED Wert zurück. 
  
Wenn **QueryInterface** einen angeforderten Schnittstellenzeiger zurückgibt, muss auch die Referenzanzahl des neuen Objekts erhöht werden. Die Referenzanzahl eines Objekts ist ein numerischer Wert, der zum Verwalten der Lebensdauer des Objekts verwendet wird. Wenn die Referenzanzahl größer als 1 ist, kann der Speicher des Objekts nicht freigegeben werden, da es aktiv verwendet wird. Erst wenn die Referenzanzahl auf 0 fällt, kann das Objekt sicher losgelassen werden. 
  
Die beiden anderen **IUnknown-Methoden** **AddRef** und **Release** verwalten die Referenzanzahl. **AddRef** erhöht die Referenzanzahl, während sie von **Release** verringert wird. Alle Methoden oder API-Funktionen, die Schnittstellenzeiger zurückgeben, **z. B. QueryInterface,** müssen **AddRef** aufrufen, um die Referenzanzahl zu erhöhen. Alle Implementierungen von Methoden, die Schnittstellenzeiger empfangen, müssen **"Release"** aufrufen, um die Anzahl zu dekrementieren, wenn der Zeiger nicht mehr benötigt wird. **Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0. 
  
> [!NOTE]
> Da **AddRef** und **Release** keine genauen Werte zurückgeben müssen, dürfen Aufrufer dieser Methoden die Rückgabewerte nicht verwenden, um zu bestimmen, ob ein Objekt noch gültig ist oder zerstört wurde. 
  
## <a name="see-also"></a>Siehe auch



[Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

