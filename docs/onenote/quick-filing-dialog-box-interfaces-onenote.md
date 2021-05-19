---
title: Für schnelle Ablage Dialogfeld Feld Schnittstellen (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: In diesem Thema werden die Schnittstellen, die Sie zum programmgesteuerten Anpassung des Dialogfelds Quick Ablegen in OneNote 2013 verwenden können.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425337"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Für schnelle Ablage Dialogfeld Feld Schnittstellen (OneNote 2013)

In diesem Thema werden die Schnittstellen, die Sie zum programmgesteuerten Anpassung des Dialogfelds Quick Ablegen in OneNote 2013 verwenden können.
  
## <a name="quick-filing-dialog-box"></a>Dialogfeld "Schnell ablegen"

Das Dialogfeld Quick Ablegen in OneNote 2013 ist anpassbare Dialogfeld, in dem Benutzer eine Position in der Hierarchiestruktur OneNote auswählen kann. Auswählbar Speicherorte enthalten Notebooks, Abschnittsgruppen, Abschnitte, Seiten und Unterseiten. Das Dialogfeld wird sowohl in der OneNote-Anwendung und externen Anwendungen über die OneNote 2013 API verwendet. Abbildung 1 zeigt das Dialogfeld Quick Ablegen im Standardzustand.
  
**Abbildung 1. Dialogfeld für schnelle Ablage ohne Anpassungen**

![Dialogfeld "Schnell ablegen" ohne Anpassungen Schnell]ablegen(media/ON15Con_quick_filing_dialog.jpg "ohne Anpassungen")
  
Innerhalb des Dialogfelds können Benutzer die Hierarchie alle Notizbücher zum Suchen für bestimmte Standorte oder die OneNote-Struktur durch Eingabe in das Textfeld Suchen navigieren. Aspekten im Dialogfeld angepasst werden kann, gehören Titel, Beschreibung, letzte Liste "Suchergebnisse", das Kontrollkästchen Text und Zustand, Strukturtiefe, Schaltflächen und auswählbar Speicherorttypen.

Sie können die schnelle ablegen Dialogfeldfunktionen über zwei OneNote 2013 Schnittstellen zugreifen. Die **IQuickFilingDialog** -Schnittstelle ermöglicht es Benutzern, instanziieren, einrichten, und führen das Dialogfeld. Die **IQuickFilingDialogCallback** -Schnittstelle wird aufgerufen, nachdem das Dialogfeld geschlossen wird. Das Dialogfeld in der OneNote-Prozess ausgeführt wird, sodass ein Mechanismus benötigt werden, um das Dialogfeld Thread ausgeführt weiter und dann die Auswahl des Benutzers als auch den Status des Dialogfelds erfasst werden, wenn er geschlossen ist. 
  
## <a name="iquickfilingdialog-interface"></a>IQuickFilingDialog-Schnittstelle
<a name="odc_IQuickFilingDialog"> </a>

Diese Schnittstelle ermöglicht es dem Benutzer anpassen, und führen Sie das Dialogfeld. Der Benutzer kann ein Dialogfeld über die **Application** -Klasse instanziiert werden mithilfe der **Application.QuickFilingDialog** -Methode. Die Methode gibt eine Instanz des Dialogfelds zurück. Nachdem Sie die Eigenschaften des Dialogfelds festgelegt sind, wird die **IQuickFilingDialog.Run** -Methode das Dialogfeld ausgeführt. Diese Methode wird das Dialogfeld in einem neuen Thread ausgeführt. 
  
**Eigenschaften**

|**Name**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Dient zum Abrufen oder wird der Titeltext, der angezeigt wird in der Titelleiste des Fensters Feld Dialogfeld.  <br/> |
|**Description** <br/> |string  <br/> |Dient zum Abrufen oder Festlegen der Textbeschreibung und was Sie wählen den Benutzer auffordern. Dieser Wert kann mehrere Zeilen Text sein.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Ruft ab oder legt den Text, der das Kontrollkästchen bildet. Wenn dieser Wert auf eine nicht leere Zeichenfolge festgelegt ist, wird ein Kontrollkästchen im Dialogfeld angezeigt. Wenn der Wert auf eine leere Zeichenfolge ist, wird kein Kontrollkästchen angezeigt.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Dient zum Abrufen oder Festlegen des Status des Kontrollkästchens. Wenn der Wert auf **false** festgelegt ist, ist das Kontrollkästchen deaktiviert, wenn das Dialogfeld gestartet wird. Wenn der Wert auf **true** festgelegt ist, ist das Kontrollkästchen aktiviert, wenn das Dialogfeld gestartet wird solange **CheckboxText** eine nicht leere Zeichenfolge ist.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Ruft die ID Handle des Fensters Feld Dialogfeld Quick ablegen.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Ruft ab oder legt fest, wie tief die OneNote-Struktur im Abschnitt alle Notizbücher angezeigt werden soll. Standardmäßig ist die Struktur bis zu den Abschnitten angezeigt. Diese Eigenschaft wirkt sich nicht auf welche Typen von Elementen ausgewählt werden kann. <br/> Wenn **TreeDepth** auf ein Element festgelegt ist der weiter unten in der OneNote-Hierarchie als von eine der Schaltflächen ausgewählt werden kann, wird die Tiefe angezeigte Struktur der niedrigste mögliche auswählbar Element. D. h., wenn Strukturtiefe festgelegt wird, dass nach unten zu Seiten angezeigt, aber das niedrigste auswählbare-Element ein Abschnitt ist, die Struktur nach unten zu Abschnitten angezeigt.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Dient zum Abrufen oder Festlegen der Handle-ID des übergeordneten Fensters des Dialogfelds. Wenn diese Eigenschaft festgelegt ist, werden im Dialogfeld für die schnelle ablegen an die zugewiesene übergeordnetes Fenster modal, wenn das Dialogfeld wird geöffnet. D. h., werden Benutzer nicht auf das übergeordnete Fenster zugreifen, bis das Dialogfeld Quick ablegen geschlossen wird.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Dient zum Abrufen oder Festlegen der Position des Fensters in Bezug auf dem Bildschirm. Standardmäßig wird das Dialogfeld in der Mitte des übergeordneten Fensters oder auf dem Desktop angezeigt.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Ruft die Objekt-ID des OneNote-Speicherorts, die vom Benutzer ausgewählt werden, wenn das Dialogfeld geschlossen wird. Wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, wird das Objekt festgelegt auf Null.  <br/> |
|**PressedButton** <br/> |ulong  <br/> |Ruft ab, welche Schaltfläche geklickt wurde, wenn das Dialogfeld geschlossen wurde. Wenn die Schaltfläche **Abbrechen** geklickt wurde, gibt diese Eigenschaft den Wert-1 zurück. Alle anderen Schaltflächen werden Werte für ganze Zahl im Bereich von 0, um 1 für jede Schaltfläche hinzugefügt, um das Dialogfeld erhöht zugewiesen. Der Integer-Wert, der die Standardschaltfläche **OK** ist 0.  <br/> |
   
### <a name="methods"></a>Methoden

**SetRecentResults**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Legt fest, welche Ergebnisliste der zuletzt verwendeten im Dialogfeld Quick ablegen angezeigt wird, und gibt an, ob einige besondere Einreichung Speicherorten in der Liste enthalten. Benutzer können eine Ergebnisliste der zuletzt verwendeten aus der [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) -Enumeration auswählen. Benutzer können auch die folgenden Optionen zur Liste hinzufügen: aktuellen Abschnitt, die aktuelle Seite oder abgelegte Notizen. Wenn **RecentResultType.rrtNone** ausgewählt ist, wird keine Ergebnisliste der zuletzt verwendeten angezeigt.  <br/> |
|**Syntax** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Parameter** <br/> | _recentResults_ &ndash; Ein Objekt vom Typ **RecentResultType,** das angibt, welche aktuelle Ergebnisliste angezeigt werden soll. Wenn **rrtNone** ausgewählt ist, wird keine Ergebnisliste der zuletzt verwendeten im Dialogfeld angezeigt.<br/><br/>  _fShowCurrentSection_ &ndash; Ein boolescher Wert, der angibt, ob der aktuelle Abschnitt in die aktuelle Ergebnisliste aufgenommen werden soll.<br/><br/>  _fShowCurrentPage_ &ndash; Ein boolescher Wert, der angibt, ob die aktuelle Seite in die aktuelle Ergebnisliste aufgenommen werden soll.<br/><br/>  _fShowUnfiledNotes_ &ndash; Ein boolescher Wert, der angibt, ob der Abschnitt "Unbereinigt" in die Liste der zuletzt verwendeten Ergebnisse aufgenommen werden soll.  <br/> |
   
> [!NOTE]
> [!HINWEIS] Wenn Sie ein speziellen Einreichung Speicherort mithilfe einer der Schaltflächen im Dialogfeld aktiviert werden kann, wird es nicht in der Liste angezeigt. Wenn kein Element ausgewählt werden in der Ergebnisliste der zuletzt geöffneten gefunden wird, wird keine Ergebnisliste der zuletzt verwendeten angezeigt. 
  
Das folgende Beispiel verwendet die **SetRecentResults** -Methode des aktuellen Abschnitts, OneNote und aktuelle Seite in der Ergebnisliste der zuletzt geöffneten angezeigt. 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

**AddButton**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht Benutzern das Hinzufügen und Schaltflächen im Dialogfeld anpassen. Benutzer können Geben Sie den Text auf die Schaltflächen und welche Elemente der OneNote-Hierarchie von jede Schaltfläche ausgewählt werden können.  <br/> |
|**Syntax** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Parameter** <br/> | _bstrText_ &ndash; Eine Zeichenfolge, die den Text angibt, der auf der Schaltfläche angezeigt werden soll. Um die Standardschaltfläche **OK** anzupassen, übergeben Sie einen null-Wert als **bstrText**.  <br/><br/>_allowedElements_ &ndash; Ein **HierarchyElement-** Element, das angibt, welche nicht schreibgeschützten OneNote Hierarchieelemente, die ein Benutzer mithilfe der Schaltfläche auswählen darf. Für die Auswahl mehrere Elemente, sollte der Benutzer für alle Uint äquivalente **HierarchyElement** Typen als eine **HierarchyElement** zulässig Operators **OR** übergeben.<br/><br/>  _allowedReadOnlyElements_ &ndash; Ein **HierarchyElement,das** angibt, OneNote schreibgeschützte Hierarchieelemente, die ein Benutzer mithilfe der Schaltfläche auswählen darf. Für die Auswahl mehrere Elemente, sollte der Benutzer nach allen Werten **Uint** -Entsprechungen **HierarchyElement** Typen als eine **HierarchyElement** zulässig Operators **OR** übergeben.<br/><br/>  _fDefault_ &ndash; Ein boolescher Wert, der angibt, ob diese Schaltfläche die Standardschaltfläche sein soll. Wenn mehrere Schaltflächen als Standard festgelegt sind, wird die letzte angegebene Schaltfläche die Standardschaltfläche.  <br/> |
   
Im folgenden Beispiel wird das Dialogfeld Quick ablegen drei Schaltflächen hinzugefügt. Das erste aus, die **alle**, kann von allen Elementen in der Hierarchiestruktur OneNote ausgewählt werden. Andere, **Notebooks** und **Seiten** anzeigen, können ausgewählt werden nur, wenn ihre entsprechenden Elemente, Notebooks und Seiten, ausgewählt sind.
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

**Run**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Zeigt das Dialogfeld Quick ablegen, von einem neuen Thread an. Es erfordert einen Verweis auf die **IQuickFilingDialogCallback** -Schnittstelle, deren **OnDialogClosed** -Methode aufgerufen wird, sobald das Dialogfeld wird geschlossen.  <br/> |
|**Syntax** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Parameter** <br/> | _piCallback_ &ndash; Ein Verweis auf die **IQuickFilingDialogCallback-Schnittstelle,** die instanziiert wird, sobald das Dialogfeld geschlossen wird.  <br/> |
   
Im folgenden Beispiel wird mithilfe die **Run** -Methode das Dialogfeld Quick Ablegen von einem neuen Thread an. 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

**TreeCollapsedState**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Gibt an, ob die Hierarchiestruktur erweitert oder reduziert werden.  <br/> |
|**Syntax** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Parameter** <br/> | _tcs_ - gibt an, ob die Struktur erweitert oder reduziert ist.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Filtert die Liste der Notizbücher nach Typ dargestellt.  <br/> |
|**Syntax** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Parameter** <br/> | _nfo_ - gibt den Satz von Notebooks, die aus der Liste gefiltert werden sollen  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Die Option neue Notizbuch erstellen in das Dialogfeld angezeigt.  <br/> |
|**Syntax** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Parameter** <br/> |Keines  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Fügt einen Benutzer als ersten-Editor in ein Notizbuch in das Dialogfeld Quick ablegen.  <br/> |
|**Syntax** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Parameter** <br/> | _initialEditor_ - die e-Mail-Adresse des Benutzers, die Sie als Editor in das Notizbuch hinzufügen möchten. Wenn das Notizbuch über das Dialogfeld für schnelle Ablage erstellt wird, wird es automatisch für alle ursprünglichen Editoren freigegeben.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Entfernt alle ursprüngliche Editoren aus dem Dialogfeld Quick ablegen.  <br/> |
|**Syntax** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Parameter** <br/> |Keine  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Zeigt den Hyperlink Hilfethema Freigabe im Dialogfeld Quick ablegen.  <br/> |
|**Syntax** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Parameter** <br/> |Keine  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>IQuickFilingDialogCallback-Schnittstelle
<a name="odc_IQuickFilingDialog"> </a>

Diese Schnittstelle ermöglicht es dem Benutzer auf die Eigenschaften des Dialogfelds zugreifen, nachdem das Dialogfeld wird geschlossen. Nachdem das Dialogfeld wird geschlossen, ruft OneNote 2013 die **IQuickFilingDialogCallback.OnDialogClose** -Methode in dieser Schnittstelle. 
  
Eine Klasse, die diese Schnittstelle erbt muss definiert werden.
  
### <a name="methods"></a>Methoden

Im folgende Abschnitt werden die Schnittstellen im zuvor zugeordneten Methoden beschrieben.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Ermöglicht Benutzern das Hinzufügen von Funktionen zum Erfassen und verwenden Sie die Auswahl des Benutzers aus dem Dialogfeld. Diese Methode wird aufgerufen, nachdem das Dialogfeld Quick ablegen geschlossen wurde. Diese Methode ist eine Funktion, die **IQuickFilingDialogCallback** Schnittstellen definieren.  <br/> |
|**Syntax** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Parameter** <br/> | _Dialog_ &ndash; Das **IQuickFilingDialog-Objekt,** das die **OnDialogClose-Methode aufgerufen** hat.  <br/> |
   
Das folgende Beispiel ist ein Beispiel **IQuickFilingDialogCallback** -Schnittstelle. Die **OnDialogClose** -Methode wird die Auswahl des Benutzers aus dem Dialogfeld Quick Ablegen in der Konsole gedruckt. 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a>Beispiel
<a name="odc_IQuickFilingDialog"> </a>

Im folgenden Codebeispiel wird ein Dialogfeld Quick ablegen, die eine angepasste Titel, Beschreibung, letzte Ergebnisliste, Strukturtiefe, das Kontrollkästchen und Schaltflächen hat geöffnet. Des Benutzers ausgewähltes Element, gedrückt, und das Kontrollkästchen Statusdienst in einem Konsolenfenster angezeigt werden, wenn das Dialogfeld geschlossen wird. Um die Seitenschaltfläche aktiviert angezeigt wird, verfügt der Benutzer zum Suchen nach einer Seite, und wählen Sie ihn, da die Strukturtiefe nach unten zu Abschnitten festgelegt ist. Das Dialogfeld ist kein untergeordnetes Element des Fensters.
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a>Siehe auch

- [OneNote-Entwicklerreferenz](onenote-developer-reference.md)

