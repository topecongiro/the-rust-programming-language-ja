--- a/src/doc/book/unsafe.md
+++ b/src/doc/book/unsafe.md
@@ -4,7 +4,7 @@ Rust’s main draw is its powerful static guarantees about behavior. But safety
 checks are conservative by nature: there are some programs that are actually
 safe, but the compiler is not able to verify this is true. To write these kinds
 of programs, we need to tell the compiler to relax its restrictions a bit. For
-this, Rust has a keyword, `unsafe`. Code using `unsafe` has less restrictions
+this, Rust has a keyword, `unsafe`. Code using `unsafe` has fewer restrictions
 than normal code does.
 
 Let’s go over the syntax, and then we’ll talk semantics. `unsafe` is used in
@@ -41,8 +41,8 @@ unsafe impl Scary for i32 {}
 ```
 
 It’s important to be able to explicitly delineate code that may have bugs that
-cause big problems. If a Rust program segfaults, you can be sure it’s somewhere
-in the sections marked `unsafe`.
+cause big problems. If a Rust program segfaults, you can be sure the cause is
+related to something marked `unsafe`.
 
 # What does ‘safe’ mean?
 
@@ -100,7 +100,7 @@ that you normally can not do. Just three. Here they are:
 
 That’s it. It’s important that `unsafe` does not, for example, ‘turn off the
 borrow checker’. Adding `unsafe` to some random Rust code doesn’t change its
-semantics, it won’t just start accepting anything. But it will let you write
+semantics, it won’t start accepting anything. But it will let you write
 things that _do_ break some of the rules.
 
 You will also encounter the `unsafe` keyword when writing bindings to foreign
diff --git a/src/doc/book/unsized-types.md b/src/doc/book/unsized-types.md
