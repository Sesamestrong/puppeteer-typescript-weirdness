# Typescript puppeteer problem

This repo is the result of running

```sh
npm install puppeteer
npm install --save-dev @types/puppeteer
```

and populating `tsconfig.json` and a `src/` directory. Running `tsc` causes it to give me the following error:

```
node_modules/@types/puppeteer/index.d.ts:55:46 - error TS2304: Cannot find name 'Element'.

55 export type WrapElementHandle<X> = X extends Element ? ElementHandle<X> : X;
                                                ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:89:56 - error TS2304: Cannot find name 'Element'.

89     $eval<R>(selector: string, pageFunction: (element: Element) => R | Promise<R>): Promise<WrapElementHandle<R>>;
                                                          ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:104:33 - error TS2304: Cannot find name 'Element'.

104         pageFunction: (element: Element, x1: UnwrapElementHandle<X1>) => R | Promise<R>,
                                    ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:122:33 - error TS2304: Cannot find name 'Element'.

122         pageFunction: (element: Element, x1: UnwrapElementHandle<X1>, x2: UnwrapElementHandle<X2>) => R | Promise<R>,
                                    ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:143:22 - error TS2304: Cannot find name 'Element'.

143             element: Element,
                         ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:166:33 - error TS2304: Cannot find name 'Element'.

166         pageFunction: (element: Element, ...args: any[]) => R | Promise<R>,
                                    ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:180:58 - error TS2304: Cannot find name 'Element'.

180     $$eval<R>(selector: string, pageFunction: (elements: Element[]) => R | Promise<R>): Promise<WrapElementHandle<R>>;
                                                             ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:195:34 - error TS2304: Cannot find name 'Element'.

195         pageFunction: (elements: Element[], x1: UnwrapElementHandle<X1>) => R | Promise<R>,
                                     ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:213:34 - error TS2304: Cannot find name 'Element'.

213         pageFunction: (elements: Element[], x1: UnwrapElementHandle<X1>, x2: UnwrapElementHandle<X2>) => R | Promise<R>,
                                     ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:234:23 - error TS2304: Cannot find name 'Element'.

234             elements: Element[],
                          ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:257:34 - error TS2304: Cannot find name 'Element'.

257         pageFunction: (elements: Element[], ...args: any[]) => R | Promise<R>,
                                     ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:826:42 - error TS2304: Cannot find name 'Element'.

826 export interface ElementHandle<E extends Element = Element> extends JSHandle<E>, Evalable {
                                             ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:826:52 - error TS2304: Cannot find name 'Element'.

826 export interface ElementHandle<E extends Element = Element> extends JSHandle<E>, Evalable {
                                                       ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2364:26 - error TS2304: Cannot find name 'Element'.

2364     queryOne?: (element: Element | Document, selector: string) => Element | null;
                              ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2364:36 - error TS2304: Cannot find name 'Document'.

2364     queryOne?: (element: Element | Document, selector: string) => Element | null;
                                        ~~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2364:67 - error TS2304: Cannot find name 'Element'.

2364     queryOne?: (element: Element | Document, selector: string) => Element | null;
                                                                       ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2365:26 - error TS2304: Cannot find name 'Element'.

2365     queryAll?: (element: Element | Document, selector: string) => Element[] | NodeListOf<Element>;
                              ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2365:36 - error TS2304: Cannot find name 'Document'.

2365     queryAll?: (element: Element | Document, selector: string) => Element[] | NodeListOf<Element>;
                                        ~~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2365:67 - error TS2304: Cannot find name 'Element'.

2365     queryAll?: (element: Element | Document, selector: string) => Element[] | NodeListOf<Element>;
                                                                       ~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2365:79 - error TS2304: Cannot find name 'NodeListOf'.

2365     queryAll?: (element: Element | Document, selector: string) => Element[] | NodeListOf<Element>;
                                                                                   ~~~~~~~~~~

node_modules/@types/puppeteer/index.d.ts:2365:90 - error TS2304: Cannot find name 'Element'.

2365     queryAll?: (element: Element | Document, selector: string) => Element[] | NodeListOf<Element>;
                                                                                              ~~~~~~~


Found 21 errors.
```
