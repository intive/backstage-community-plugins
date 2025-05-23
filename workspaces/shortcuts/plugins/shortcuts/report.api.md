## API Report File for "@backstage-community/plugin-shortcuts"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { ApiRef } from '@backstage/core-plugin-api';
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { IconComponent } from '@backstage/core-plugin-api';
import { JSX as JSX_2 } from 'react/jsx-runtime';
import { Observable } from '@backstage/types';
import { Shortcut as Shortcut_2 } from '@backstage-community/plugin-shortcuts';
import { ShortcutApi as ShortcutApi_2 } from '@backstage-community/plugin-shortcuts';
import type { StorageApi } from '@backstage/core-plugin-api';

// @public
export class DefaultShortcutsApi implements ShortcutApi_2 {
  constructor(storageApi: StorageApi);
  // (undocumented)
  add(shortcut: Omit<Shortcut_2, 'id'>): Promise<void>;
  // (undocumented)
  get(): Shortcut_2[];
  // (undocumented)
  getColor(url: string): string;
  // (undocumented)
  remove(id: string): Promise<void>;
  // (undocumented)
  shortcut$(): Observable<Shortcut_2[]>;
  // (undocumented)
  update(shortcut: Shortcut_2): Promise<void>;
}

// @public @deprecated (undocumented)
export const LocalStoredShortcuts: typeof DefaultShortcutsApi;

// @public (undocumented)
export type Shortcut = {
  id: string;
  url: string;
  title: string;
};

// @public (undocumented)
export interface ShortcutApi {
  add(shortcut: Omit<Shortcut, 'id'>): Promise<void>;
  get(): Shortcut[];
  getColor(url: string): string;
  remove(id: string): Promise<void>;
  shortcut$(): Observable<Shortcut[]>;
  update(shortcut: Shortcut): Promise<void>;
}

// @public (undocumented)
export const Shortcuts: (props: ShortcutsProps) => JSX_2.Element;

// @public (undocumented)
export const shortcutsApiRef: ApiRef<ShortcutApi>;

// @public (undocumented)
export const shortcutsPlugin: BackstagePlugin<{}, {}, {}>;

// @public
export interface ShortcutsProps {
  // (undocumented)
  allowExternalLinks?: boolean;
  // (undocumented)
  icon?: IconComponent;
}
```
