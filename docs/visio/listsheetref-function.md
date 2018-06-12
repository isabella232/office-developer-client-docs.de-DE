---
title: LISTSHEETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Gibt eine Blattreferenz auf das Listencontainer-Shape zurück, das das Shape enthält.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797373"
---
# <a name="listsheetref-function"></a>LISTSHEETREF Function

Gibt eine Blattreferenz auf das Listencontainer-Shape zurück, das das Shape enthält.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010 
  
## <a name="syntax"></a>Syntax

LISTMEMBERCOUNT()
  
### <a name="return-value"></a>R�ckgabewert

ShapeSheet-Referenz
  
## <a name="remarks"></a>Bemerkungen

Wenn es sich bei dem Shape nicht um ein Listenelement handelt, gibt die LISTSHEETREF-Funktion #REF! zurück.
  
## <a name="example"></a>Beispiel

LISTSHEETREF(1)!Height 
  
Gibt den Werte in der Zelle "Height" des Listencontainer-Shapes zurück, das das Shape enthält. 
  

