---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330219"
---
# <a name="adrparm"></a>ADRPARM

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Anzeige und das Verhalten des Dialogfelds allgemeine Adresse. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Elemente

**cbABContEntryID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die von **lpABContEntryID**verwiesen wird.
    
**lpABContEntryID**
  
> Zeiger auf die Eintrags-ID des Containers, der die anfängliche Liste der Empfängeradressen bereitstellt, die im Dialogfeld Adresse angezeigt werden.
    
**ulFlags**
  
> Bitmaske der Flags, die verschiedenen Optionen für Adress Dialogfelder zugeordnet sind. Die folgenden Flags können festgelegt werden:
    
AB_RESOLVE
  
> Aktivieren Sie alle Namen, die aufgelöst werden sollen, nachdem das Dialogfeld Adresse geschlossen wurde. Wenn es zu mehrdeutigen Einträgen kommt, die aus dem Prozess der Namensauflösung resultieren, wird ein Dialogfeld angezeigt, in dem der Benutzer Hilfe beim Auflösen auffordert. Durch Festlegen dieses Flags wird sichergestellt, dass alle von [IAddrBook:: Address](iaddrbook-address.md) zurückgegebenen Namen aufgelöst werden. 
    
AB_SELECTONLY
  
> Deaktivieren Sie das Erstellen von einmaligen Adressen für eine Empfängerliste. Dieses Flag wird nur verwendet, wenn das Dialogfeld modal ist, wie durch das festgelegte DIALOG_MODAL-Flag angegeben.
    
ADDRESS_ONE
  
> Der Benutzer kann aus einer Liste genau einen Empfänger anstelle mehrerer Empfänger auswählen. Dieses Flag ist nur gültig, wenn **cDestFields** NULL ist und das Dialogfeld modal ist, wie durch das festgeLEGTe DIALOG_MODAL-Flag angegeben. 
    
DIALOG_MODAL
  
> Bewirkt, dass die modale Version des Dialogfelds allgemeine Adresse angezeigt wird. Entweder dieses Flag oder DIALOG_SDI sollte festgelegt werden; Sie können nicht beide festgelegt werden. 
    
DIALOG_OPTIONS
  
> Bewirkt, dass die Schaltfläche " **Sendeoptionen** " im Dialogfeld angezeigt wird. Dieses Flag wird nur verwendet, wenn das Dialogfeld modal ist, wie durch das festgelegte DIALOG_MODAL-Flag angegeben. 
    
DIALOG_SDI
  
> Bewirkt, dass die nicht modale Version des Dialogfelds allgemeine Adresse angezeigt wird. Entweder dieses Flag oder DIALOG_MODAL sollte festgelegt werden; Sie können nicht beide festgelegt werden. Das DIALOG_SDI-Flag wird für nicht-Outlook-Clients ignoriert, und die modale Version des Dialog Felds wird angezeigt. Daher sollte im _lpulUIParam_ -Parameter von [IAddrBook:: Address](iaddrbook-address.md)kein Zeiger auf ein Handle erwartet werden.
    
**lpReserved**
  
> Reserviert, muss NULL sein.
    
**ulHelpContext**
  
> Gibt den Kontext in der **Hilfe** an, der zuerst angezeigt wird, wenn der Benutzer im Dialogfeld Adresse auf die Schaltfläche Hilfe klickt. 
    
**lpszHelpFileName**
  
> Zeiger auf den Namen einer Hilfedatei, die dem Dialogfeld Adresse zugeordnet wird. Das **lpszHelpFileName** -Element wird zusammen mit **ulHelpContext** verwendet, um die Windows- **WinHelp** -Funktion aufzurufen. 
    
**lpfnABSDI**
  
> Zeiger auf eine MAPI-Funktion, die auf dem [ACCELERATEABSDI](accelerateabsdi.md) -Prototyp oder NULL basiert. Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben. Clients, die eine **ADRPARM** -Struktur an [IAddrBook:: Address](iaddrbook-address.md) erstellen, müssen das **LPFNABSDI** -Element immer auf NULL festlegen. Wenn das DIALOG_SDI-Flag festgelegt ist, wird es von MAPI vor dem zurückgeben auf eine gültige Funktion festgelegt. Clients rufen diese Funktion in der Meldungsschleife auf, um sicherzustellen, dass Beschleuniger im Dialogfeld Adressbuch funktionieren. Wenn das Dialogfeld geschlossen wird und MAPI die Funktion aufruft, auf die durch das **lpfnDismiss** -Element verwiesen wird, sollten Clients die Hookfunktion der **ACCELERATEABSDI** -Funktion aus ihrer Meldungsschleife aufheben. 
    
**lpfnDismiss**
  
> Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS](dismissmodeless.md) -Prototyp oder NULL basiert. Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben. MAPI Ruft die **DISMISSMODELESS** -Funktion auf, wenn der Benutzer das Dialogfeld "nicht modale Adresse" abschließt und einen Client anruft, der **IAddrBook:: Address** angibt, dass das Dialogfeld nicht mehr aktiv ist. 
    
**lpvDismissContext**
  
> Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS** -Funktion übergeben werden sollen, auf die durch das **lpfnDismiss** -Element verwiesen wird. Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben. 
    
**lpszCaption**
  
> Zeiger auf Text, der als Titel für das Dialogfeld Allgemeine Adresse verwendet werden soll.
    
**lpszNewEntryTitle**
  
> Zeiger auf Text, der als Schaltflächenbeschriftung für die Schaltfläche verwendet werden soll, mit der das Dialogfeld **neuer Eintrag** oder ein anderes Dialogfeld aufgerufen wird. 
    
**lpszDestWellsTitle**
  
> Zeiger auf Text, der als Titel für die Empfänger Textfeld-Steuerelemente verwendet werden kann, die in der modalen Version des Dialogfelds allgemeine Adresse angezeigt werden können. Dieses Element wird nicht für nicht modale Dialogfelder verwendet. 
    
**cDestFields**
  
> Anzahl der Empfänger Textfeld-Steuerelemente in der modalen Version des Dialogfelds Adresse oder NULL, wenn das Dialogfeld nicht aktiviert ist. Das Dialogfeld Adresse kann nur geöffnet werden, wenn die folgenden Bedingungen zutreffen: 
    
  - Das **cDestFields** -Element wird auf NULL festgelegt. 
    
  - Das DIALOG_BOX-Flag wird festgelegt.
    
  - Das ADDRESS_ONE-Flag wird nicht festgelegt.
    
  Festlegen von **cDestFields** auf 0XFFFFFFFF impliziert, dass MAPI die Standardanzahl von Empfänger Textfeld-Steuerelemente erstellen soll. In diesem Fall müssen die **lppszDestTitles** -und **LPULDESTCOMPS** -Member NULL sein. 
    
**nDestFieldFocus**
  
> Gibt das Textfeld-Steuerelement an, das den anfänglichen Fokus haben soll, wenn die modale Version des Dialogfelds angezeigt wird. Dieser Wert muss zwischen 0 und dem Wert von **cDestFields** minus 1 liegen. 
    
**lppszDestTitles**
  
> Zeiger auf ein Array von Bezeichnungen für Schaltflächen, die den einzelnen Textfeld-Steuerelementen zugeordnet sind, die in der modalen Version des Dialogfelds Adresse angezeigt werden. Der Wert des **cDestFields** -Elements gibt die Anzahl der im Array enthaltenen Bezeichnungen an. Wenn das **lppszDestTitles** -Element NULL ist, verwendet die **Address** -Methode Standardtitel. 
    
**lpulDestComps**
  
> Zeiger auf ein Array von Empfängertyp Werten wie MAPI_TO, MAPI_CC und MAPI_BCC, das jedem Textfeld-Steuerelement zugeordnet ist. Der Wert des **CDestFields** -Elements gibt die Anzahl der im Array enthaltenen Empfängertypen an. Die Werte, auf die durch **lpulDestComps** verwiesen wird, können zum Festlegen der **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft jedes Empfängers verwendet werden. Wenn das **lpulDestComps** -Element NULL ist, verwendet die **Address** -Methode Standardempfänger Typen. 
    
**lpContRestriction**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die den Typ von Adresseinträgen einschränkt, die im Dialogfeld angezeigt werden können. 
    
**lpHierRestriction**
  
> Zeiger auf eine **SRestriction** -Struktur, die die Adressbuchcontainer einschränkt, die Adresseinträge angeben können, die im Dialogfeld angezeigt werden sollen. 
    
## <a name="remarks"></a>Bemerkungen

**ADRPARM** -Strukturen werden von Clients und Dienstanbietern verwendet, um die Darstellung und das Verhalten der MAPI-Dialogfelder für allgemeine Adressen zu steuern. Im Dialogfeld Adresse gibt es zwei Varianten: moduslos und modal. Einige der Elemente in der **ADRPARM** -Struktur gelten für beide Versionen des Dialogfelds, einige gelten jedoch nur für eine der beiden Versionen. In der folgenden Tabelle sind die Elemente einer **ADRPARM** -Struktur mit den allgemeinen Adress Dialogfeldern verknüpft. 
  
|ADRPARM-Element|Dialogfeldtyp|
|:-----|:-----|
|**cbABContEntryID** und **lpABContEntryID** <br/> |Modal und ohne Modus  <br/> |
|**ulFlags** <br/> |Modal und ohne Modus  <br/> |
|**lpReserved** <br/> |Modal und ohne Modus  <br/> |
|**ulHelpContext** und **lpszHelpFileName** <br/> |Modal und ohne Modus  <br/> |
|**lpfnABSDI** <br/> |MODELESS  <br/> |
|**lpfnDismiss** und **lpvDismissContext** <br/> |MODELESS  <br/> |
|**lpszCaption** <br/> |Modal und ohne Modus  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**und **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal und ohne Modus  <br/> |
|**lpHierRestriction** <br/> |Modal und ohne Modus  <br/> |
   
Das Dialogfeld nicht modal ist eine schreibgeschützte Anzeige von Einträgen aus einem oder mehreren Adressbuch Containern. Im Dialogfeld können alle Einträge aus den ausgewählten Containern angezeigt werden oder auf nur die Einträge und Container beschränkt werden, die Kriterien erfüllen, die mit einer Einschränkung festgelegt wurden. Die Inhaltseinschränkung, auf die durch **lpContRestriction** verwiesen wird, kann die Art der angezeigten Einträge einschränken, und die Hierarchieeinschränkung, auf die durch **lpHierRestriction** verwiesen wird, kann die Container einschränken, die die Einträge bereitstellen. Um den Anrufer zu benachrichtigen, wenn das Dialogfeld geschlossen wird, ruft MAPI eine Funktion auf, die vom Anrufer bereitgestellt wird, der dem [DISMISSMODELESS](dismissmodeless.md) -Prototyp entspricht. Eine andere Funktion, die mit dem [ACCELERATEABSDI](accelerateabsdi.md) -Prototyp übereinstimmt, wird von MAPI bereitgestellt und vom Aufrufer in der Windows-Meldungsschleife aufgerufen, um das Arbeiten mit Tastenkombinationen zu erleichtern. Die nicht modale Version des Dialogfelds MAPI-Adresse kann angezeigt werden, wenn Clients [IAddrBook:: Address](iaddrbook-address.md) aufrufen oder wenn Dienstanbieter [IMAPISupport:: Address](imapisupport-address.md)aufrufen. 
  
Das modale Dialogfeld ist eine Lese-/Schreibzugriff Anzeige von Einträgen aus einem oder mehreren Containern. Der Inhalt kann auf dieselbe Weise beeinflusst werden wie die nicht modale Version durch Einschränkungen, die in den **lpContRestriction** -und **lpHierRestriction** -Membern festgelegt sind. Zusätzlich zum Listenfeld, das Container Einträge anzeigt, kann das modale Dialogfeld zwischen einem und drei Textfeld-Steuerelemente enthalten, um vom Benutzer ausgewählte Einträge zu halten. Jedes Bearbeitungssteuerelement ist einem bestimmten Empfängertyp oder einer **PR_RECIPIENT_TYPE** -Eigenschaft wie MAPI_TO zugeordnet. Das Dialogfeld modal address kann von einer der **Adress** Methoden angezeigt werden oder wenn Clients IAddrBook aufrufen [::D ails](iaddrbook-details.md) und Dienstanbieter rufen [IMAPISupport::D ails](imapisupport-details.md). 
  
Diese Abbildung enthält zwei Textfeld-Steuerelemente, da das **cDestFields** -Element der **ADRPARM** -Struktur, die die Anzeige dieses Dialogfelds steuert, auf 2 festgelegt ist. Das erste Steuerelement hat den anfänglichen Fokus, da das **nDestFieldFocus** -Element auf 0 festgelegt ist. 
  
Das **lpszNewEntryTitle** -Element zeigt auf Text für eine Schaltflächenbeschriftung, die, wenn es ausgewählt wird, ein zusätzliches Dialogfeld angezeigt wird. In der Regel wird, wie in der Abbildung des Dialogfelds modal angezeigt, die Schaltfläche **neu** beschriftet, und im daraufhin angezeigten Dialogfeld werden alle Adresstypen aufgelistet, die von einem beliebigen Adressen Anbieter im Profil erstellt werden können. Clients führen dazu, dass dieses Dialogfeld für den **neuen Eintrag** angezeigt wird, indem [IAddrBook:: neuer Eintrag](iaddrbook-newentry.md) aufgerufen wird und NULL für den Parameter _CbEidNewEntryTpl_ und NULL für den _lpEidNewEntryTpl_ -Parameter übergeben wird, wenn der Benutzer die Schaltfläche auswählt. Die in diesem Dialogfeld enthaltenen Informationen stammen aus der einmaligen MAPI-Tabelle. 
  
Jeder Eintrag in diesem Dialogfeld ist mit einer Vorlage verknüpft, um die Daten einzugeben, die zum Erstellen einer Adresse des jeweiligen Typs erforderlich sind. Die meisten Adressbuchanbieter stellen eine Vorlage für jede Art von Adresseintrag bereit, die Sie erstellen können. Wenn ein Benutzer über dieses Dialogfeld eine Auswahl trifft, zeigt MAPI die entsprechende Vorlage an.
  
Die wichtigsten vier Bits des **ulFlags** -Elements der **ADRPARM** -Struktur enthalten eine Versionsnummer, die die Version der **ADRPARM** -Struktur identifiziert. Die aktuelle Version ist 0 (null) oder ADRPARM_HELP_CTX. Die aktuelle MAPI-Implementierung schlägt für eine andere Version der Struktur als NULL fehl. 
  
Zukünftige Versionen der Struktur können vollständig unterschiedlich sein; Sie unterstützen möglicherweise nicht die Struktur der Version-Zero. Die folgenden Makros werden zum Extrahieren der Versionsnummer aus dem **ulFlags** -Element und zur Kombination mit den definierten Flags bereitgestellt: 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Siehe auch

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

